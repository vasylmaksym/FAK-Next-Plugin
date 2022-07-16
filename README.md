# FAK-Next-Plugin

## Actions

| $hook_name  | $callback | $priority | $accepted_args |                         description                         |
| ----------- | --------- | --------- | -------------- | ----------------------------------------------------------- |
| woocommerce_product_data_panels | add_tab_fields | - | - |  |
| woocommerce_process_product_meta | save_options | - | - | save selected mix and match or optional products to meta data |
| woocommerce_before_add_to_cart_button | display_options_on_product_page | - | - | render product mix and match or optional products from backoffice (if exists) |
| woocommerce_add_to_cart_validation | validate_selected_options | 10 | 2 | validate selected options (mix and match / optional) |
| woocommerce_add_cart_item_data | save_selected_options | 10 | 2 | save selected options (mix and match/ optional in cart meta data) |
| woocommerce_new_order_item | display_selected_options_with_order_info | 1 | 3 |  |
| woocommerce_before_calculate_totals | add_option_price_on_checkout | 99 | - |  |
| woocommerce_created_customer | backoffice_user_pass | 10 | 3 | set user password from backoffice if exists (migration functionality) |
| woocommerce_before_add_to_cart_button | fak_external_comment_field | - | - | render comment form on WC single product page |
| woocommerce_checkout_create_order_line_item | fak_add_custom_order_line_item_meta | 10 | 4 | add comment (if exists) to order meta data |
| woocommerce_checkout_process | wc_minimum_order_amount | - | - | check if order sum >= 1 € (by default) |
| woocommerce_order_item_meta_start | thank_page_show_variables | 10 | 4 | show variable || mix and match products on order thank page |
| woocommerce_after_checkout_validation | woocommerce_after_checkout_validation_update | 9999 | 2 | - |
| woocommerce_before_add_to_cart_form | fak_before_add_to_cart_form | - | - | render variations or accessories products on WC single product page if enabled options |
| woocommerce_after_checkout_form | fak_oddt_datepicker_js | 10 | - | wp_enqueue_script datepicker.js |
| woocommerce_checkout_before_customer_details | fak_oddt_echo_fields | 10 | 1 | render delivery date time fields |
| woocommerce_checkout_update_order_meta | fak_oddt_save_meta | 10 | 1 | save selected date/time to order meata data |
| woocommerce_checkout_process | fak_oddt_validate | - | - | validate selected date/time values |
| woocommerce_admin_order_data_after_billing_address | fak_oddt_display_admin_order_meta | 10 | 1 | show selected date/time values in admin page after billing address |
| woocommerce_thankyou | fak_oddt_view_order_and_thankyou_page | 20 | - | show selected date/time values on thankyou page |
| woocommerce_view_order | fak_oddt_view_order_and_thankyou_page | 20 | - | show selected date/time values on view order page |
| woocommerce_checkout_update_order_review | fak_oddt_woocommerce_checkout_update_order_review | 10 | 1 | just update WC session |
| woocommerce_checkout_update_order_meta | woocommerce_checkout_update_order_meta_order_number | 10 | 2 | order number from backoffice |
| woocommerce_email_order_details | woocommerce_email_order_details_order_number | 1 | 4 |show backoffice order number |
| woocommerce_order_status_pending_to_on-hold_notification | set_fak_order_number | 10 | 2 | backoffice ON |
| woocommerce_order_status_pending_to_processing_notification | set_fak_order_number | 10 | 2 | backoffice ON |
| woocommerce_email_order_details | woocommerce_email_order_details_show_oddt_info | 2 | 4 | show order delivery date time in email |
| woocommerce_before_shop_loop | oddt_render_filters_form | 1 | - | render order delivery date time filter form |
| woocommerce_no_products_found | oddt_no_products_found | - | - | call woocommerce_before_shop_loop action |
| woocommerce_single_product_summary | replace_single_add_to_cart_button | 1 | - | check if product allow after filters (only if filters selected) |
| woocommerce_new_order | unset_session | - | - | just refresh session |
| woocommerce_check_cart_items | checkout_processing_time_message | - | - | product unavaliable after filters (show message) |
| woocommerce_single_variation | custom_product_button | 20 | - | replace add to cart button (only if product unavaliable after ODDt filters) |
| woocommerce_single_product_summary | custom_product_button | 30 | - | replace add to cart button (only if product unavaliable after ODDt filters) |
| woocommerce_single_variation | hurry_up_message | 20 | - | show hurry up message (only if use stock system) |
| woocommerce_single_product_summary | hurry_up_message | 20 | - | show hurry up message (only if use stock system) |
| woocommerce_single_variation | out_of_stock_message | 20 | - | show out of stock message (only if use stock system) |
| woocommerce_single_product_summary | out_of_stock_message | 30 | - | show out of stock message (only if use stock system) |
