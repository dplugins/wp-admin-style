# WP Admin Style
## Elements oriented CSS Framework. UI Components for Building WordPress Plugins.

It is intended to replace default WordPress styling and to help us unify all our plugins.

1. To start inclide dist/wp-admin-style.css
2. Wrap your deside with wp-admin-style class

```
<div class="wp-admin-style">
// Your code here
</div>
```

or attach wp-admin-style to the body

```
<body class="wp-admin-style">
// Your code here
</body>
```

WordPress Filter to attach the body class
```
function wpast_body_classes( $classes ) {
    global $post;

    $classes[] = 'wp_admin_style';  // add custom class to all single posts    
     
    // if ( is_singular( 'post' ) ) {  
    //     $classes[] = 'wp_admin_style';  // add custom class to all single posts
    // }
     
    // if ( is_singular( 'page' ) ) {  
    //     $classes[] = 'wp_admin_style';  // add custom class to all single pages
    // }   
     
    // if ( is_singular( 'customposttype' ) ) {  // change customposttype to your CPT slug
    //     $classes[] = 'wp_admin_style';  // add custom class to all single custom post types
    // }       
     
    // if ( is_home() ) {  
    //     $classes[] = 'wp_admin_style';  // add custom class to blog homepage
    // }           
     
    // if ( is_front_page() ) { 
    //     $classes[] = 'wp_admin_style';  // add custom class to blog static page frontpage
    // }               
     
    // if ( is_archive() ) { 
    //     $classes[] = 'wp_admin_style';  // add custom class to archive pages
    // }                   
 
    return $classes;
}
add_filter( 'body_class', 'wpast_body_classes' );
```

## What WP Admin Style is not?
Front end framework for websites. We do not want to bloat it with bells and wisless that website needs. We want to optimise components for only WordPress plugins backend.

[Link to the Official website](https://wpadminstyle.com/)