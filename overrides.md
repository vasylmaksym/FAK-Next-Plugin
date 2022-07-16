# FAK-Next-Plugin

## Actions

| $hook_name | $callback: description |
| ---------- | ---------------------- |
| `woocommerce_product_data_panels` | `add_tab_fields`: - |
| `woocommerce_process_product_meta` | `save_options`: save selected mix and match or optional products to meta data |
| `woocommerce_before_add_to_cart_button` | `display_options_on_product_page`: render product mix and match or optional products from backoffice (if exists) |
| `woocommerce_add_to_cart_validation` | `validate_selected_options`: validate selected options (mix and match / optional) |
| `woocommerce_add_cart_item_data` | `save_selected_options`: save selected options (mix and match/ optional in cart meta data) |
| `woocommerce_new_order_item` | `display_selected_options_with_order_info`: - |
| `woocommerce_before_calculate_totals` | `add_option_price_on_checkout`: - |
| `woocommerce_created_customer` | `backoffice_user_pass`: set user password from backoffice if exists (migration functionality) |
| `woocommerce_before_add_to_cart_button` | `fak_external_comment_field`: render comment form on WC single product page |
| `woocommerce_checkout_create_order_line_item` | `fak_add_custom_order_line_item_meta`: add comment (if exists) to order meta data |
| `woocommerce_checkout_process` | `wc_minimum_order_amount`: check if order sum >= 1 € (by default) |
| `woocommerce_order_item_meta_start` | `thank_page_show_variables`: show variable or mix and match products on order thank page |
| `woocommerce_after_checkout_validation` | `woocommerce_after_checkout_validation_update`: - |
| `woocommerce_before_add_to_cart_form` | `fak_before_add_to_cart_form`: render variations or accessories products on WC single product page if enabled options |
| `woocommerce_after_checkout_form` | `fak_oddt_datepicker_js`: wp_enqueue_script datepicker.js |
| `woocommerce_checkout_before_customer_details` | `fak_oddt_echo_fields`: render delivery date time fields |
| `woocommerce_checkout_update_order_meta` | `fak_oddt_save_meta`: save selected date/time to order meata data |
| `woocommerce_checkout_process` | `fak_oddt_validate`: validate selected date/time values |
| `woocommerce_admin_order_data_after_billing_address` | `fak_oddt_display_admin_order_meta`: show selected date/time values in admin page after billing address |
| `woocommerce_thankyou` | `fak_oddt_view_order_and_thankyou_page`: show selected date/time values on thankyou page |
| `woocommerce_view_order` | `fak_oddt_view_order_and_thankyou_page`: show selected date/time values on view order page |
| `woocommerce_checkout_update_order_review` | `fak_oddt_woocommerce_checkout_update_order_review`: just update WC session |
| `woocommerce_checkout_update_order_meta` | `woocommerce_checkout_update_order_meta_order_number`: order number from backoffice |
| `woocommerce_email_order_details` | `woocommerce_email_order_details_order_number`: show backoffice order number |
| `woocommerce_order_status_pending_to_on-hold_notification` | `set_fak_order_number`: backoffice ON |
| `woocommerce_order_status_pending_to_processing_notification` | `set_fak_order_number`: backoffice ON |
| `woocommerce_email_order_details` | `woocommerce_email_order_details_show_oddt_info`: show order delivery date time in email |
| `woocommerce_before_shop_loop` | `oddt_render_filters_form`: render order delivery date time filter form |
| `woocommerce_no_products_found` | `oddt_no_products_found`: call woocommerce_before_shop_loop action |
| `woocommerce_single_product_summary` | `replace_single_add_to_cart_button`: check if product allow after filters (only if filters selected) |
| `woocommerce_new_order` | `unset_session`: just refresh session |
| `woocommerce_check_cart_items` | `checkout_processing_time_message`: product unavaliable after filters (show message) |
| `woocommerce_single_variation` | `custom_product_button`: replace add to cart button (only if product unavaliable after ODDt filters) |
| `woocommerce_single_product_summary` | `custom_product_button`: replace add to cart button (only if product unavaliable after ODDt filters) |
| `woocommerce_single_variation` | `hurry_up_message`: show hurry up message (only if use stock system) |
| `woocommerce_single_product_summary` | `hurry_up_message`: show hurry up message (only if use stock system) |
| `woocommerce_single_variation` | `out_of_stock_message`: show out of stock message (only if use stock system) |
| `woocommerce_single_product_summary` | `out_of_stock_message`: show out of stock message (only if use stock system) |
| `woocommerce_single_product_summary` | `single_product_summary_validate`: only if stock system is enabled: validate product, required subproducts, mix and match and variables subproducts |
| `woocommerce_after_checkout_validation` | `checkout_stock_validation`: stock system: validate all products in cart backend part |
| `woocommerce_check_cart_items` | `checkout_stock_validation_view`: stock system: validate all products in cart frontend part |
| `woocommerce_after_cart_item_quantity_update` | `update_options_cart_item_data`: stock system: revalidate all products in cart after change quantity products |
| `woocommerce_rest_insert_product_cat` | `on_save_termmeta`: update _category_last_update term meta |
| `pre_delete_term` | `update_products_status`: set products to draft if they have only 1 category and we deled it |
| `woocommerce_checkout_update_order_meta` | `action_woocommerce_new_order`: send order to strapi |
| `woocommerce_created_customer` | `action_woocommerce_created_customer`: send order to strapi |
| `woocommerce_payment_complete` | `action_payment_complete`: send order to strapi |
| `woocommerce_order_status_failed` | `action_order_status_cancelled`: send order to strapi |
| `woocommerce_order_status_cancelled` | `action_order_status_cancelled`: send order to strapi |
| `woocommerce_order_status_completed` | `action_order_status_completed`: send order to strapi |

## Filters

| $hook_name  | $callback: description |
| ----------- | ---------------------- |
| `woocommerce_product_data_tabs` | `add_product_tab`: add new tab "custom options" |
| `woocommerce_get_item_data` | `display_selected_options_on_checkout`: render selecte options on checkout page |
| `woocommerce_add_cart_item_data` | `fak_add_item_data`: add value from comment form to cart item data |
| `woocommerce_get_item_data` | `fak_add_item_meta`: display information as meta on cart page |
| `woocommerce_email_enabled_customer_new_account` | `check_if_need_send_email`: not send email customers from backoffice after migration |
| `woocommerce_cart_item_quantity` | `wc_cart_item_quantity`: set product quantity from product meta data |
| `woocommerce_get_price_html` | `fak_wc_price_per_piece`: per piece text in price |
| `woocommerce_add_cart_item_data` | `cart_mix_and_match_item`: split mix and match products in cart |
| `woocommerce_checkout_fields` | `woocommerce_checkout_fields_update`: just add class to billing fields |
| `woocommerce_is_purchasable` | `filter_is_purchasable`: hide price for logged in users (if option is enabled) |
| `woocommerce_get_price_html` | `show_price_for_logged_in_users_only`: hide price for logged in users (if option is enabled) |
| `woocommerce_related_products` | `fak_backoffice_related_products`: show related products from backoffice |
| `woocommerce_product_tabs` | `fak_variations_products_tabs`: add variations products tab if option is enabled |
| `woocommerce_product_tabs` | `fak_accessories_products_tabs`: add accessories products tab if option is enabled |
| `woocommerce_product_tabs` | `fak_maintenance_products_tabs`: add maintenance products tab if option is enabled |
| `woocommerce_display_product_attributes` | `filter_additional_info_tabs`: remove allergenner and ingridienten tabs (if option is enabled) |
| `the_content` | `customizing_woocommerce_description`: add allergenen to description if exists |
| `wc_order_statuses` | `add_fak_invoice_to_order_statuses`: register FAK Invoice order status |
| `woocommerce_payment_gateways` | `add_fak_invoice_gateway_class`: register FAK Invoice payment method |
| `woocommerce_package_rates` | `fak_oddt_woocommerce_package_rates`: validate shipping zone |
| `woocommerce_thankyou_order_received_text` | `woocommerce_thankyou_order_received_text_order_number`: show backoffice order number |
| `woocommerce_email_subject_new_order` | `custom_subject_for_new_order`: add backoffice order number |
| `woocommerce_email_heading_new_order` | `fak_filter_email_heading_new_order`: replace WC order number -> backoffice order number in email heading |
| `woocommerce_order_again_cart_item_data` | `filter_woocommerce_order_again_cart_item_data`: WC order again - set mix_and_match, variables subproducts |
| `wc_get_price_decimals` | `fak_price_decimals`: set decimals 2 if decimals < 2 (for correct price showing) |
| `woocommerce_product_get_price` | `fak_product_get_price`: calculate price based on customer pricelists |
| `woocommerce_variation_prices_price` | `fak_get_variation_product_price`: calculate price based on customer pricelists |
| `woocommerce_get_variation_prices_hash` | `fak_variation_product_price_hash`: update price hash |
| `woocommerce_product_variation_get_price` | `fak_get_variation_price`: calculate price based on customer pricelists |
| `woocommerce_related_products` | `assortment_wc_related_products`: show products for customer based on pricelists settings |
| `woocommerce_product_get_catalog_visibility` | `dynamically_change_product_visibility`: show products for customer based on pricelists settings |
| `woocommerce_cart_item_permalink` | `no_webshop_wc_cart_item_permalink`: change product permalink |
| `woocommerce_order_item_permalink` | `no_webshop_wc_order_item_permalink`: change product permalink |
| `posts_where` | `assortment_posts_where`: get products based on customer pricelists |
| `get_terms` | `assortment_wc_change_term_counts`: get categories based on customer pricelists |
| `posts_where` | `oddt_where`: modify query: get products based on ODDT filter |
| `posts_orderby` | `oddt_orderby`: modify query: get products based on ODDT filter |
| `woocommerce_loop_add_to_cart_link` | `oddt_maybe_disable`: disable dd to cart button if product not match by ODDT filter |
| `woocommerce_add_cart_item_data` | `options_cart_item_data`: add options (mix and match/variable) to cart item data |
| `woocommerce_add_to_cart_validation` | `add_to_cart_stock_validation`: stock system validate product |
| `update_post_metadata` | `filter_function_name_3113`: update product attributes metadata |
| `woocommerce_rest_prepare_product_cat` | `get_category`: update categories api data attributes |
| `woocommerce_loop_add_to_cart_link` | `change_add_to_cart_link`: update button for mix and match products |
| `woocommerce_registration_error_email_exists` | `wc_invalid_link_filter`: - |
| `woocommerce_attribute_label` | `rename_weight_attribute`: rename attribute |
| `woocommerce_variation_option_name` | `add_gram_to_weight`: - |
| `woocommerce_loop_add_to_cart_link` | `mix_and_match_add_to_cart_button`: update button for mix and match products |
| `woocommerce_new_product` | `on_new_product`: update product options |
| `woocommerce_update_product` | `on_update_product`: update product options |
| `woocommerce_quantity_input_args` | `set_minimum_quantity`: minimum quantity from backoffice |
| `woocommerce_add_to_cart_validation` | `wc_add_to_cart_quantity_validation`: validate quantity |