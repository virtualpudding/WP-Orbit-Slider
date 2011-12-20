=== WP Orbit Slider ===

Contributors: Jonny Janiero ( Virtual Pudding )
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZY92BLQVS5BSS
Tags: orbit, orbit slider, slideshow, promotions, slider, javascript slider, jquery slider, carousel, featured content, gallery, banners, image rotation, images, rotate, auto, autoplay, shortcode, slide, media, pictures, custom post types, thumbnails, responsive
Requires at least: 3.0
Tested up to: 3.2
Stable Tag: 1.0

WP Orbit Slider is a jQuery slider that uses a custom post type for each slide. Oh, its also responsive!


== Description ==

Promotion slider is a jQuery slider that makes it easy to insert a simple slideshow, or implement multiple rotating ad zones, on a webpage.  Because it is highly-customizable, you are in complete control of what shows on the slider, what shows on your promotion pages and how it all works.  A simple options page and straight-forward shortcodes provide great flexibility to the average user, while power users can take advantage of special actions and filters built into the plugin to add their own customizations.

[youtube http://www.youtube.com/watch?v=z5Zz0GK-9G0]

You can easily create promotions in the WordPress admin area; complete with a title, content and image.  The image displays in the slider, and when a user clicks on the image, they are taken to the full promotion page.  Designed with SEO in mind, this slider can be integrated anywhere on your blog or website.

[Install this plugin now!](http://coveredwebservices.com/wp-plugin-install/?plugin=promotion-slider)

This plugin features: 

* Easy creation and management of promotions within the WordPress admin.
* Automatic inclusion of featured images attached to promotions.
* Creation of unique pages with a unique URL for each promotion.
* SEO friendly jQuery animation that can be viewed on most mobile devices.
* Slider navigation that makes it easy for users to find and click on the promotion of their choice.
* A selection of different default styles to choose from.
* Supports the option to link to external URLs instead of promotion pages from the slider.
* Optionally display third party ad code in a slider panel.
* Ability to display only a certain post type or limit to posts from a certain category.
* Customizable time delay and the ability to disable automatic slide advancement.
* Built-in support for displaying a title and/or excerpt for each post or promotion.
* The ability to display multiple sliders on a single page without conflicts.
* Works with any custom post type.
* Plenty of hooks available to advanced WordPress users.

This plugin is provided as-is, but [paid support for this plugin is available](http://www.orderofbusiness.net/request-quote/).

If you have feature requests for this plugin, [please let us know](http://www.orderofbusiness.net/contact-us/plugin-feedback/)!


== Installation ==

1. Upload the `wp-orbit-slider` folder to the `/wp-content/plugins/` directory.
2. Go to the 'Plugins' page of your WordPress administration area and activate the plugin.
3. Use the shortcode `[orbit-slider]` in the content area of a page or post where you want the image slider to appear.
4. Create your slides by clicking on 'Slides' in your administration menu and selecting 'Add New Slide'.  *The slider uses ONLY the featured image attached to any given promotion.*


== Frequently Asked Questions ==

= How do I insert the Orbit Slider? =

You can insert the Orbit Slider by pasting the shortcode `[orbit-slider]` into the content area of a page or post.  **Be sure to use the HTML editor when inserting shortcodes!**  Also, be aware that if you don't have any published slides, the slider will not appear.  To customize your slider, there are optional attributes that can be used with the shortcode.

= What are the optional attributes that can be used with the shortcode? = 

There are several attributes that are supported by the `[orbit-slider]` shortcode:


1. **category** - You can choose to display only posts from a particular category. Please note that if a category doesn't exist, all posts will show in the slider as default.  Example: `[orbit-slider category="my-category"]`
2. **numberposts** - The numberposts attribute allows you to set the number of posts to display in the slider.  The default is -1 and will show all available posts. Example: `[orbit-slider numberposts="3"]`


You can combine all of these attributes together as needed.  Example: `[promoslider category="my_category" numberposts="3"]`

= How do I create Slides? =

Slides can be created in the WordPress administration area by clicking on 'Slides' menu in the navigation and then selecting 'Add New Slide'.  

You will be able to provide a title, content (or caption), category, and optonal URL, as well as a featured image.  
Images can be placed within the content area of the slide but will remain unresponsive inside (unless .

You can optionally create categories for your promotions by clicking on 'Promotions' in the navigation area and then selecting 'Categories'.  You can create sliders that will only display certain categories using the shortcode attributes.

= How can I enable the display of additional content in the slider? =

You can enable the title and/or excerpt display from the slider options page.  The 'Slider Options' page is under 'Promotions' in the left hand navigation in the WordPress admin area.  You can also enable the display of the title and/or excerpt using the shortcode attributes.

Enabling the excerpt while the default slider navigation is active will result in some overlap of the two elements.  I would recommend switching to the navigation links instead. You can also disable the slider navigation altogether from here if you wish.

Note: By using the 'id' attribute in the shortcode, you can assign all instances of the promotion slider a unique id.  This will allow you to customize the look and feel of individual sliders by editing the css in your theme's stylesheet.

More advanced users might want to display extra content on one slider, but not on another.  This can be done by using the id attribute available in the shortcode and using the action hooks to add custom functions.  Here is an example:

>	`function my_slider_content($values){
	  extract($values);
	  if( $id == 'my_unique_id' ){
		add_action('promoslider_content', 'promoslider_display_title', 9);
		add_action('promoslider_content', 'promoslider_extra_content');
	  }
	}
	add_action('promoslider_content', 'my_slider_content');
	function promoslider_extra_content(){
	  echo '<< INSERT CUSTOM CONTENT HERE >>';
	}`
>

= How can I change the time delay between slides? =

Just click on 'Promotions' in the WordPress admin area and select the 'Slider Options' page.  You can change the default time delay for all your sliders from here.  To change the time delay for just one instance of a slider, just use the shortcode attributes described previously.

= What if I don't want the slides to automatically advance? =

If you would rather not have the slides advance automatically, users can still browse through the promotions in the slider with the slider navigation.  To disable the automatic advancement of slides, just click on 'Promotions' in the WordPress admin area and select the 'Slider Options' page.  You can disable automatic slide advancement from here.  To change the automatic advancement for just one instance of a slider, just use the shortcode attributes described previously.

= What if I want to show the slider in my sidebar? =

All you need to do is add a text widget to your sidebar and include the shortcode as described earlier.  Most likely, you will need to adust the height of the slider in your sidebar by using the shortcode attribute.  You may also want to use a more space-saving navigation option, or remove the slider navigation altogether.

= What if I don't want to use the shortcode?  Can I hardcode the slider into my theme? =

Hardcoding the slider into your theme is just as simple as using the shortcode.  All you do is insert the following line into your theme where you want the slider to appear:

>`<?php echo do_shortcode('[promoslider]') ?>`

If you want to use any of the shortcode attributes when hardcoding your theme, you may do so like this:

>`<?php echo do_shortcode('[promoslider id="my_id" post_type="post" category="my_category"]'); ?>`

= Can I control the order in which the slides appear? =

By default, the slides appear in order by publication date.  You can change the order by changing the publish date for a promotion.  This is the simplest way, but you can also use the more advanced method below.

We provide a filter which allows you to customize the get_posts() query.  You can use any of the [documented parameters](http://codex.wordpress.org/Template_Tags/get_posts#Parameters:_WordPress_2.6.2B) in your query.  Here is an example of how you could control the order:

>	`function order_promotions_by_title($query){
	  $query['orderby'] = 'title';
	  $query['order'] = 'ASC';
	  return $query;
	}
>	add_filter('promoslider_query', 'order_promotions_by_title');

= How can I change the default linking behaviour for a slider panel? = 

When creating or editing a promotion, you can easily change the linking behaviour for that particular promotion from the meta box displayed below the content editing area.  You can have the links open in a new window, define a custom destination URL and disable the links altogether.

= How can I insert third party ad code into the slider? = 

You can easily insert ad code into the slider by using the meta box below the content editing area when creating or editing a promotion in the WordPress admin.  There is a box where you can insert your third party code and a checkbox which will make it actively display for that particular promotion.  We recommend only using this feature when you know the exact size of the ads that will appear.

= What hooks do you provide in this plugin? =

Here is a list of all the hooks available to advanced users:

1. **before_promoslider** - This action hook is called just before each instance of the Promotion Slider within a wrapper div.  The id of the slider is passed as an argument.  The id will be null if it is not set for a particular slider.
2. **after_promoslider** - This action hook is called just after each instance of the Promotion Slider within a wrapper div. The id of the slider is passed as an argument.  The id will be null if it is not set for a particular slider.
3. **promoslider_content** - This action hook is called within each panel in the Promotion Slider.  We use this hook to populate the content in the slider, including the title, excerpt and image.  The $values argument is available when using this hook and is an array containing the following variables: $id (the HTML id attribute for the current slider), $title (the post title), $excerpt (the post excerpt), $image(the HTML image element for the current post's featured image), $destination_url (the destination URL for the post), $target (the HTML anchor target attribute to be used with the destination URL), $disable_links (a boolean variable that is true when a user wishes to disable all links for a particular post), $display_title (a string indicating whether to show the title and, if so, which one), and $display_excerpt (a string indicating whether to show the excerpt or not).  Reference the shortcode attributes for acceptable values for display_title and display_excerpt.
4. **promoslider_nav** - This action hook is called after all the panels and before the closing div tag for the slider, but only if there is more than one panel and the thumbnail navigation is not being used.  We use this hook to insert the slider navigation. $display_nav is passed as an argument.  See the shortcode attribute for acceptable values.
5. **promoslider_thumbnail_nav** - This action hook is called just before the 'before_promoslider' hook after the slider and before the closing wrapper div tag.  We use this hook to insert the slider thumbnail navigation. Several values are passed as an array: $id(the HTML id attribute for the current slider), $title(the post title), $thumbs(a collection of thumbnails to be used for the navigation) and $width(used to match the thumbnail nav witdth to that of the slider).
6. **promoslider_query** - This filter is applied to the get_posts() query for each slider before it is run.  This hook can only be used to make changes to all the sliders on the site because the $query variable is all that is passed as an argument.
7. **promoslider_query_by_id** - This filter is applied to the get_posts() query before it is run and after the promoslider_query filter.  The argument passed to this filter is an associative array containg the query and id.  You can use the PHP extract() function to easily gain access to the $query and $id variables.  Be sure to return the $query within an associative array at the end of your filter.  The purpose of this filter is to allow you to change the query for a slider with a particular id.
8. **promoslider_custom_query_results** - This filter allows you to return the results object of your own custom query.  The purpose of this filter is so users can bypass the get_posts() function and run more advanced custom queries.
9. **promoslider_image_size** - This filter allows you to change the default image size in the slider.  The default value is the string 'full'.  The value passed through this filter is directly applied to the $size argument in the get_the_post_thumbnail() function.  See the WordPress codex for more information on acceptable values and functionality.
10. **promoslider_image_size_by_id** - This filter allows you to change the default image size in the slider based on the slider's id.  This filter passes an associative array containing the $id and $image_size values.  The $image_size must be returned within an associative array.  The value passed through this filter is directly applied to the $size argument in the get_the_post_thumbnail() function.  See the WordPress codex for more information on acceptable values and functionality.
11. **promoslider_thumb_size** - This filter allows you to change the default thumbnail size used in the slider thumbnail navigation.  The default value is the string 'thumbnail'.  The value passed through this filter is directly applied to the $size argument in the get_the_post_thumbnail() function.  See the WordPress codex for more information on acceptable values and functionality.
12. **promoslider_add_meta_to_save** - This filter is applied to the data array prior to processing and saving the promotion meta data.  It is designed for developers who need to save additional meta data to the promotion custom post type after having created a custom meta box.  The $data variable is available when using this filter and contains an array of all the meta keys to be saved when a promotion is created or updated.

== Screenshots ==

1. An example of the Promotion Slider with a default installation.
2. An example of the Promotion Slider with the title display enabled.  This slider is using the default styling for the title.
3. An example of the Promotion Slider with some minor customizations.  By following the instructions in the FAQ section, you can make your customizations upgrade-proof.
4. An example of the Promotion Slider using the alternate navigation links.
5. A look at the 'add new promotion' screen.  You can see options available under the promotions menu item on the left.  The 'Set featured image' link on the bottom right is how you upload an image to the slider.

== Changelog ==

= 1.0 =
* Birth of another plugin.
