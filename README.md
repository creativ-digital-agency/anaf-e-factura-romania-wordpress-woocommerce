=== e-Factura for WooCommerce ===
Contributors: creativdigital
Tags: woocommerce, anaf, efactura, invoice, romania
Requires at least: 5.8
Tested up to: 6.9
Stable tag: 1.0.2
Requires PHP: 7.4
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Integrates WooCommerce with the Romanian ANAF e-Factura (SPV) system. Generate UBL 2.1 XML invoices and submit them directly to ANAF.

== Description ==

**e-Factura for WooCommerce** is a free, open-source plugin that connects your WooCommerce store directly to the Romanian ANAF e-Factura system (SPV - Spațiul Privat Virtual).

Starting January 2024, all B2B transactions in Romania require electronic invoicing through the ANAF system. This plugin automates the entire process without requiring expensive third-party SaaS subscriptions.

= Key Features =

* **Direct ANAF Integration** - Connect via official OAuth2 API using your ANAF digital certificate
* **Auto-Pilot Mode** - Automatically generate and send invoices when orders are marked as "Completed"
* **UBL 2.1 XML Generation** - Creates invoices compliant with RO-CIUS (Romanian Core Invoice Usage Specification)
* **Status Monitoring** - Background checks for invoice validation status from ANAF
* **ANAF Response Download** - Automatically downloads the official signed ZIP response from ANAF
* **B2B Checkout Fields** - Adds CUI/CIF, Registration Number, IBAN, and Sector fields to checkout
* **Test Mode** - Sandbox environment support for testing before going live
* **HPOS Compatible** - Works with WooCommerce High-Performance Order Storage

= How It Works =

1. Configure your company details (CUI, Company Name)
2. Register your application on the ANAF portal and obtain Client ID/Secret
3. Connect the plugin to ANAF using your digital certificate
4. Enable Auto-Pilot or manually generate invoices from the order screen
5. The plugin handles XML generation, upload, status checking, and response download

= Requirements =

* WooCommerce 5.0 or higher
* PHP 7.4 or higher
* A valid ANAF SPV account
* A qualified digital certificate registered with ANAF
* Your application registered on [ANAF Developer Portal](https://pfinternet.anaf.ro)

= Documentation =

For detailed setup instructions, please refer to:

* [ANAF OAuth Registration Guide](https://static.anaf.ro/static/10/Anaf/Informatii_publice/OAuth/Oauth_procedura_inregistrare_aplicatii_portal_ANAF.pdf)
* [RO e-Factura Technical Guide](https://mfinante.gov.ro/web/efactura)

= Support =

This plugin is developed and maintained by [Creativ Digital Agency](https://creativdigital.ro).

For support inquiries, please contact us at: **office@creativdigital.ro**

We respond to all support requests within 48 hours during business days.

== Installation ==

1. Upload the plugin files to `/wp-content/plugins/e-factura-for-woocommerce/` or install via WordPress plugins screen
2. Activate the plugin through the 'Plugins' screen in WordPress
3. Navigate to **WooCommerce > RO e-Factura** to configure

= ANAF Application Setup =

1. Go to [ANAF Portal](https://pfinternet.anaf.ro) > Dezvoltatori Aplicații > Adaugă aplicație
2. Set the **Redirect URI** to: `https://yoursite.com/wp-admin/admin.php?page=wc-efactura-ro`
3. Copy the generated **Client ID** and **Client Secret**
4. Enter these credentials in the plugin settings and click "Save"
5. Click "Connect to ANAF" and authorize using your digital certificate

== Frequently Asked Questions ==

= Do I need a digital certificate? =

Yes. Authorization with ANAF requires a valid Qualified Digital Certificate (token) registered in your SPV account.

= Is this plugin free? =

Yes, this plugin is completely free and open-source. It connects directly to ANAF without any third-party services or subscriptions.

= Does it work with the ANAF test environment? =

Yes. Enable "Test Mode (Sandbox)" in the settings to use the ANAF test API before going live with production invoices.

= What invoice format does it generate? =

The plugin generates UBL 2.1 XML invoices compliant with the RO-CIUS (Romanian Core Invoice Usage Specification) standard required by ANAF.

= Can I use it for B2C invoices? =

The plugin is primarily designed for B2B invoicing as required by Romanian law. B2C invoices can be generated but may not require submission to ANAF depending on current regulations.

= What happens if ANAF rejects an invoice? =

The plugin monitors invoice status and adds notes to the order when an invoice is validated or rejected. If rejected, you can review the error, correct the data, and regenerate/resubmit.

== Screenshots ==

1. Plugin settings page with connection status and configuration options
2. Order metabox for manual invoice generation and ANAF submission
3. Checkout page with additional B2B fields (CUI, Registration Number)

== Changelog ==

= 1.0.2 =
* Fixed text domain to match plugin slug (e-factura-for-woocommerce)
* WordPress.org Plugin Directory compliance improvements

= 1.0.1 =
* Security hardening (nonce verification, output escaping)
* Added automatic invoice sending on order completion (Auto-Pilot)
* Improved PHPCS compliance for WordPress.org standards
* Fixed text domain for translations

= 1.0.0 =
* Initial release
* OAuth2 authentication with ANAF SPV
* UBL 2.1 XML invoice generation
* Manual and automatic invoice submission
* Status checking and ZIP download
* Checkout fields for B2B data

== Upgrade Notice ==

= 1.0.2 =
Text domain fix for WordPress.org compliance. Recommended for all users.

= 1.0.1 =
Security update with improved nonce verification and automatic sending feature. Recommended for all users.

== Privacy Policy ==

This plugin:

* Stores OAuth tokens securely in your WordPress database
* Sends invoice data directly to ANAF (no third-party servers)
* Does not collect or transmit any data to the plugin developers
* Stores generated XML files and ANAF responses in your wp-content/uploads folder

For more information about how ANAF handles your data, please refer to the [ANAF Privacy Policy](https://www.anaf.ro/anaf/internet/ANAF/informatii_publice/politica_de_confidentialitate).
