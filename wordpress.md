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