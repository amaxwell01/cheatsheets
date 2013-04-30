## Plugins
* Advanced Custom Fields
* Simple Page Ordering
* Types - Complete Solution for Custom Fields and Types

# Wordpress Snippets

## To get an image from the template
```php
<?php echo bloginfo('template_url'); ?>/images/logo.png
<?php get_bloginfo('template_url'); ?>/images/logo.png
```


## Get a posts link
```php
<?php get_permalink(); ?>
```

## [Advanced Custom Fields Snippets](http://www.advancedcustomfields.com/resources/getting-started/code-examples/)
```php
<p><?php the_field('field_name'); ?></p>
$variable = get_field('field_name');
```

## Basic default wordpress loop
```php
<?php if (have_posts()) : ?>
    <?php while (have_posts()) : the_post(); ?>
        <h1><?php the_title(); ?></h1>
        <article>
            <?php the_content(); ?>
        </article>
    <?php endwhile; ?>
<?php endif; ?>
```

## Custom WP_Query with custom taxonomy
```php
$wp_query = new WP_Query( array(
    'post_type' => 'content_blocks',
    'posts_per_page' => -1,
    'tax_query' => array(
        array(
            'taxonomy' => 'content_blocks_categories',
            'field' => 'slug',
            'terms' => 'home_slide'
        )
    )
));
```

## How to get the current page's page_id
```php
$page_id = get_the_ID();
```

## How to get the current page's category
```php
$the_page = get_the_ID();
$category = get_the_category( $the_page );
$category[0]->category_nicename === 'potential_project'
```


## How to debug the current page's content and metadata
```php
$the_page = get_the_ID();
echo var_dump( get_page( $the_page ) );
```


## How to find and replace code in MySQL
```mysql
UPDATE wp_posts SET post_content = REPLACE(post_content, 'http://website.local.com', 'http://www.website.com')

UPDATE wp_postmeta SET meta_value = REPLACE(meta_value, 'http://website.local.com', 'http://www.website.com')

UPDATE wp_options SET option_value = REPLACE(option_value, 'http://website.local.com', 'http://www.website.com')
```

## How to get a list of archives by year and then by month and then by day
```php
<ul>
    <?php
    /**/
    $years = $wpdb->get_col(
        "SELECT DISTINCT YEAR(post_date)
        FROM $wpdb->posts 
        WHERE post_status = 'publish' AND post_type = 'post'
        ORDER BY post_date DESC");
    
    foreach($years as $year) :
    ?>
        <li><a href="<?php echo get_year_link($year); ?> "><?php echo $year; ?></a>

            <ul>
                <?
                    $months = $wpdb->get_col(
                        "SELECT DISTINCT MONTH(post_date)
                        FROM $wpdb->posts
                        WHERE post_status = 'publish' AND post_type = 'post' AND YEAR(post_date) = '" . $year . "' 
                        ORDER BY post_date DESC");
                    
                    foreach($months as $month) :
                ?>
                <li><a href="<?php echo get_month_link($year, $month); ?>"><?php echo date( 'F', mktime(0, 0, 0, $month) );?></a>
                
                    <ul>
                        <?
                            $days = $wpdb->get_col(
                                "SELECT DISTINCT DAY(post_date) 
                                FROM $wpdb->posts 
                                WHERE post_status = 'publish' AND post_type = 'post' AND MONTH(post_date) = '".$month."' AND YEAR(post_date) = '".$year."' 
                                ORDER BY post_date DESC");
                            foreach($days as $day) :
                        ?>
                        <li><a href="<?php echo get_day_link($year, $month, $day); ?>"><?php echo $day;?></a></li>
                        <?php endforeach;?>
                    </ul>
                </li>
                <?php endforeach;?>
            </ul>
        </li>
    <?php endforeach; ?>
</ul>
```

