=== WP Orbit Slider ===


Contributors: Jonny Janiero ( Virtual Pudding )
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZY92BLQVS5BSS
Tags: orbit, orbit slider, slideshow, slider, javascript slider, jquery slider, carousel, featured content, gallery, banners, image rotation, images, rotate, auto, autoplay, shortcode, slide, media, pictures, custom post types, thumbnails, responsive
Requires at least: 3.0
Tested up to: 3.2
Stable Tag: 1.0

WP Orbit Slider is a jQuery slider that uses a custom post type for each slide and taxonomies to group slides for various post/pages. Oh, its also responsive!
*** Please be aware, you can only run one instance of the slide on any given post/page. This is a limitation of the original jQuery slider by Zurb. Until such changes, this WordPress plugin will operate in the same way ***
http://www.zurb.com/playground/orbit-jquery-image-slider


== Description ==

Wp Orbit Slider is a jQuery slider that makes it easy to insert a simple slider to your WordPress site.


This plugin features: 

* Custom post types and taxonomies.
* Responive layout
* Various slider options to customise the slider output.


== Installation ==

1. Upload the `wp-orbit-slider` folder to the `/wp-content/plugins/` directory.
2. Go to the 'Plugins' page of your WordPress administration area and activate the plugin.
3. Use the shortcode `[orbit-slider]` in the content area of a page or post where you want the image slider to appear.
4. Create your slides by clicking on 'Slides' in your administration menu and selecting 'Add New Slide'.  *As standard the slider ONLY uses the featured image attached to any given slide.*


== Frequently Asked Questions ==

= How do I insert the Orbit Slider? =
You can insert the Orbit Slider by pasting the shortcode `[orbit-slider]` into the content area of a page or post.  **Be sure to use the HTML editor when inserting shortcodes!**  Also, be aware that if you don't have any published slides, the slider will not appear.  To customize your slider, there are optional attributes that can be used with the shortcode.


= What are the optional attributes that can be used with the shortcode? = 
The attributes supported by the `[orbit-slider]` shortcode are:
1. **category** - You can choose to display only posts from a particular category. Please note that if a category doesn't exist, all posts will show in the slider as default.  Example: `[orbit-slider category="my-category"]`
2. **numberposts** - The numberposts attribute allows you to set the number of posts to display in the slider.  The default is -1 and will show all available posts. Example: `[orbit-slider numberposts="3"]`

You can combine both of these attributes together as needed.  Example: `[orbit-slider category="my_category" numberposts="3"]`


= How do I create Slides? =
Slides can be created in the WordPress administration area by clicking on 'Slides' menu in the navigation and then selecting 'Add New Slide'.  
You will be able to provide a title, content (or caption), category, and optonal URL, as well as a featured image.  
Images can be placed within the content area of the slide but will remain unresponsive inside (this involves specific css to play nicley).
You can optionally create categories for your slides by clicking on 'Slides' in the navigation area and then selecting 'Slide Categories'.  You can create sliders that will only display certain categories using the shortcode attributes.


= How can I enable the display of additional content in the slider? =
Out the box, this slider works best just using images and 'captions'. You can however insert any text or images inside any slide via the editor. Please be aware this will need specific css added to help it sing! When adding content to the slide via the text editor it generates a numerical content class that enables specific css targetting. E.g .slide-content-190.


= How can I change the animation settings? =
All animation type settings are found in the master options tab 'slider options'.
They are based on the original available options offered by the slider http://www.zurb.com/playground/orbit-jquery-image-slider


= What if I want to show the slider in my sidebar? =
All you need to do is add a text widget to your sidebar and include the shortcode as described earlier. But note, this slider does not allow multiple instances on one post/page so this approach may become problematic.


= What if I don't want to use the shortcode?  Can I hardcode the slider into my theme? =
Hardcoding the slider into your theme is just as simple as using the shortcode.  All you do is insert the following line into your theme where you want the slider to appear:

`<?php echo do_shortcode('[orbit-slider]') ?>`

If you want to use any of the shortcode attributes when hardcoding your theme, you may do so like this:

`<?php echo do_shortcode('[orbit-slider category="my_category"]'); ?>`



== Screenshots ==

To follow

== Changelog ==

= 1.0 =
* Just another WordPress plugin.
