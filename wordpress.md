## Plugins
* Advanced Custom Fields
* Simple Page Ordering
* Types - Complete Solution for Custom Fields and Types

# Wordpress Snippets

## To get an image from the template
```php
<?php echo bloginfo('template_url'); ?>/images/logo.png
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
