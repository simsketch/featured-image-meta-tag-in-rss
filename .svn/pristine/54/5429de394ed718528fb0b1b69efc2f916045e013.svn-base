<?php
/* 
Plugin Name: Featured Image Meta Tag in RSS
Plugin URI: http://talentresources.extremereach.com/image-meta-rss/index.html
Description: Add Featured Image as a meta tag in your RSS feed.
Author: Elon Zito
Version: 1.0
Author URI: http://www.extremereach.com
*/

function metaInRSS($content) {
	global $post;
	if ( has_post_thumbnail( $post->ID ) ){
		$content = '<meta property="og:image" content="' . get_the_post_thumbnail_url($post->ID) . '"/>'.$content;
	}
	return $content;
}

add_filter('the_content_feed', 'metaInRSS');

?>