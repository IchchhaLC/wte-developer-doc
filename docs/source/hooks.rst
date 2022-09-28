Using Hooks
=====

Thank You Page
do_action(‘wp_travel_engine_before_traveller_information_save’);
Fires before the billing details are saved on thank you page.

do_action(‘wp_travel_engine_after_traveller_information_save’);
Fires after the billing details are saved on thank you page.

Checkout Page
do_action('wte_bf_after_trip_name');
Fires after the trip name in the mini cart of the checkout page.

do_action(‘wp_travel_engine_before_billing_form’);
Fires before the output of the billing form on the checkout page.

do_action(‘wte_booking_before_submit_button’);
Fires before the billing form submit button on the checkout page.

do_action(‘wte_booking_after_submit_button’);
Fires after the billing form submit button on the checkout page.


Trip Archive Page
do_action(‘wp_travel_engine_trip_archive_outer_wrapper’);
Fires on the trip archive page that contains the outer wrapper div of the trip archive.

do_action(‘wp_travel_engine_trip_archive_loop_start’);
Action hook that contains the trip archive loop start.

do_action(‘wp_travel_engine_trip_archive_loop_end’);
Action hook that contains the trip archive loop end.

add_filter(‘wp_travel_engine_archive_header_sorting_options’);
Filters the archive page search bar sorting options on the trip archive page.

add_filter(‘wte_trip_archive_description_page_header’);
Filters the display of page header in the archive block.

add_filter(‘wp_travel_engine_template_banner_size’);
Filters the size of the banner in archive pages. Accepts WordPress default image sizes and images registered form add_image_size().

add_filter(‘wte_trip_archive_description_below_title’);
Controls the display of archive description in the taxonomy archive pages, Defaults to true.

do_action( 'wp_travel_engine_breadcrumb_holder' );
Hook to add content in trip archive page’s breadcrumb section.

do_action( 'wp_travel_engine_archive_header_block' );
Hook to set header block in trip archive page.

do_action( 'wp_travel_engine_archive_sidebar' );
Hook to add content to trip archive sidebar.

do_action( 'wp_travel_engine_header_filters' );
Hook to add new archive filters on trip archive page.


Trip single hooks

wte_before_single_trip
Fires before the single trip page content blocks are rendered.

Location: includes/templates/content-single-trip.php

do_action( 'wte_before_single_trip' );

Once the trip content section starts,
Hook: do_action( ‘wte_single_trip_content’ );


wte_after_single_trip
Fires after the single trip page content blocks are rendered.

Location: includes/templates/content-single-trip.php

do_action( 'wte_after_single_trip' );

wp_travel_engine_before_trip_content
Fires before the single trip page content blocks are rendered (wrapper).

Location: includes/templates/content-single-trip.php

/**
* wp_travel_engine_before_trip_content hook.
*
* @hooked trip_content_wrapper_start - 5 (outputs opening divs for the trip content)*/
do_action( 'wp_travel_engine_before_trip_content' );


wp_travel_engine_after_trip_content
Fires after the single trip page content blocks are rendered (wrapper).

Location: includes/templates/content-single-trip.php

/**
* wp_travel_engine_after_trip_content hook.
*
* @hooked trip_content_wrapper_end - 5 (outputs closing divs for the trip content)*/ 
do_action( 'wp_travel_engine_after_trip_content' );

wp_travel_engine_before_trip_tabs
Fires before the tabs on trip single page.

Location: includes/templates/single-trip/tabs-nav.php

do_action('wp_travel_engine_before_trip_tabs');

wp_travel_engine_after_trip_tabs #
Fires after the tabs on trip single page.

Location: includes/templates/single-trip/tabs-nav.php

do_action('wp_travel_engine_after_trip_tabs');
Dynamic Hooks

wte_single_before_trip_tab_{$field}
Dynamic hook that fires before the trip tab content. $field variable to be replaced by the tab key.

/**
* @hook - wte_single_before_trip_tab_{field_name}
* Dynamic hooks before Tab wrapper - for themes to hook content into.*/
do_action( "wte_single_before_trip_tab_{$field}" );
wte_single_after_trip_tab_{$field}
Dynamic hook that fires after the trip tab content. $field variable to be replaced by the tab key.

/**
* @hook - wte_single_after_trip_tab_{field_name}
* Dynamic hooks after Tab wrapper - for themes to hook content into.*/
do_action( "wte_single_after_trip_tab_{$field}" );
wp_travel_engine_before_secondary
Fires before the secondary widget area div in the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_before_secondary');
wp_travel_engine_before_trip_price
Fires before the pricing section and calendar for dates selection on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_before_trip_price');
wp_travel_engine_after_trip_price
Fires after the pricing section and calendar for dates selection on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_after_trip_price');
wp_travel_engine_before_trip_facts
Fires before the “trips info” section in the sidebar on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_before_trip_facts');
wp_travel_engine_after_trip_facts
Fires after the “trips info” section in the sidebar on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_after_trip_facts');
wp_travel_engine_before_related_posts
Hook to add section/block before the related trips section on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_before_related_posts');
wp_travel_engine_after_related_posts
Hook to add section/block after the related trips section on the trip single page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wp_travel_engine_after_related_posts');
wpte_after_travellers_input
Fires after the traveler numbers input field in the booking form on the single trip page.

Location: public/class-wp-travel-engine-template-hooks.php

do_action('wpte_after_travellers_input');
Removing template actions
Besides all of the available template hooks for a trip single page developers can also unhook any added sections/actions as per their requirements. This can be beneficial in a situation that requires modification of HTML structures and swapping actions priorities to customize the trip single page.

Applies to: class WP_Travel_Engine_Template_Hooks();

Methods: init_hook(); & init_single_trip_hooks();

Example: Removing gallery slider from trip single page.

/**
 * Removing Gallery Slider from Trip Content
 *  
 * @package Wp_Travel_Engine*/
$single_trip_hooks = WP_Travel_Engine_Template_Hooks::get_instance();
remove_action( 'wte_single_trip_content', array( $single_trip_hooks, 'display_single_trip_gallery' ), 10 );

Single Trip Page Tabs Navigation Section
Hook: do_action( ‘wp_travel_engine_before_trip_tabs’ ); //hook loads before tabs section

Single Trip Page Tabs Content Section
Hooks: do_action( ‘wte_single_before_trip_tab_{$field}’ ); //for themes to hook content before specific tab content
Dynamic hook that fires before the trip tab content. $field variable to be replaced by the tab key.

Hooks: do_action( ‘wte_single_trip_tab_content_{$field}’ );//for themes to hook content for specific tab.

Hooks: do_action( ‘wte_single_after_trip_tab_{$field}’ ); //for themes to hook content after specific tab content.
Dynamic hook that fires after the trip tab content. $field variable to be replaced by the tab key.

Where $field value varies:
For overview tab, $field = wp_editor
For itinerary tab, $field = itinerary
For cost tab, $field = cost
For dates tab, $field = dates
For review tab, $field = review
For map tab, $field = map


Hooks: do_action( ‘wp_travel_engine_after_trip_tabs’ ); // for themes to hook content after tab container
Fires after the tabs on the single trip page.

Single Trip Footer
Hooks: do_action( 'wte_single_trip_footer' );

Single Trip Rich Snippet Hook
Hooks: do_action( 'display_wte_rich_snippet' );

After the single trip content ends,
Fires after the single trip page content blocks are rendered.
Hook: do_action( 'wte_after_single_trip' );//used in plugin to get template file: 
script-templates/booking-process/wte-booking.php

After trip content
Fires after the single trip page content blocks are rendered (wrapper).
Hooks: do_action ( ‘wp_travel_engine_after_trip_content’ )// for themes to hook content after trip content

Single Trip Sidebar
Hooks: do_action( ‘wp_travel_engine_trip_sidebar’ );

do_action('wp_travel_engine_before_secondary');
Fires before the secondary widget area div in the single trip page.

do_action('wp_travel_engine_before_trip_price');
Fires before the pricing section and calendar for dates selection on the single trip page.

do_action(‘wp_travel_engine_after_trip_price');
Fires after the pricing section and calendar for dates selection on the trip single page.

do_action(‘wp_travel_engine_before_trip_facts’);
Fires before the “trips info” section in the sidebar on the single trip page.

do_action(‘wp_travel_engine_after_trip_facts;);
Fires after the “trips info” section in the sidebar on the trip single page.

do_action(‘wp_travel_engine_before_related_posts’);
Hook to add section/block before the related trips section on the trip single page.

do-action(‘wp_travel_engine_after_related_posts’);
Hook to add section/block after the related trips section on the trip single page.

Single Trip Tabs
Overview Tab
Hooks: do_action( ‘wte_single_trip_tab_content_wp_editor’ );//for themes to hook content into overview tab 

Itinerary Tab
Hooks: do_action( ‘wte_single_
trip_tab_content_itinerary’ );//for themes to hook content into itinerary tab

Cost Tab
Hooks: do_action( ‘wte_single_trip_tab_content_cost’ );//for themes to hook content into cost tab

FAQs Tab
Hooks: do_action( ‘wte_single_trip_tab_content_faqs’ );//for themes to hook content into faqs tab

Map Tab
Hooks: do_action( ‘wte_single_trip_tab_content_map’ );//for themes to hook content into map tab

Review Tab
Hooks: do_action( ‘wte_single_trip_tab_content_review’ );//for themes to hook content into review tab
