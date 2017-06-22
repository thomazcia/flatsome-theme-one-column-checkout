# flatsome-theme-one-column-checkout
Flatsome WordPress theme one column checkout via CSS


<?php
	
/*
	Include this code in your functions.php theme child.
	Inclua etse código no functions do seu tema filho.
*/
	
function flatsome__conditions__one_colum_checkout() {
	if (is_checkout()) {
	?>
	<style>
	.woocommerce-checkout .large-7,
	.woocommerce-checkout .large-5 {
		max-width: 100%;
			-webkit-flex-basis: 100%;
			-ms-flex-preferred-size: 100%;
			flex-basis: 100%;
	}
	</style>
	<?php 
	}
}
add_action( 'wp_footer', 'flatsome__conditions__one_colum_checkout', 100 );
