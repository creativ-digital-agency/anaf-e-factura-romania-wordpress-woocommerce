=== e-Factura for WooCommerce ===
Contribuitori: creativdigital

Tag-uri: woocommerce, anaf, efactura, invoice, romania

Versiune minimă necesară: 5.8

Testat până la: 6.9

Versiune stabilă: 1.0.2

Versiune PHP necesară: 7.4

Licență: GPLv2 sau ulterioară

Licență URI: http://www.gnu.org/licenses/gpl-2.0.html

Integrează WooCommerce cu sistemul ANAF e-Factura (SPV) din România. Generează facturi în format XML UBL 2.1 și le transmite direct către ANAF.

== Descriere ==
e-Factura for WooCommerce este un plugin gratuit și open-source care conectează magazinul tău WooCommerce direct la sistemul ANAF e-Factura (SPV - Spațiul Privat Virtual).

Începând cu ianuarie 2024, toate tranzacțiile B2B din România necesită facturare electronică prin sistemul ANAF. Acest plugin automatizează întregul proces fără a necesita abonamente costisitoare la platforme SaaS terțe.

= Caracteristici Principale =
Integrare Directă ANAF - Conectare prin API-ul oficial OAuth2 folosind certificatul digital ANAF.

Mod Auto-Pilot - Generare și trimitere automată a facturilor atunci când comenzile sunt marcate ca „Finalizate”.

Generare XML UBL 2.1 - Creează facturi conforme cu standardul RO-CIUS (Romanian Core Invoice Usage Specification).

Monitorizare Status - Verificări automate în fundal pentru statusul de validare al facturii de către ANAF.

Descărcare Răspuns ANAF - Descarcă automat arhiva ZIP oficială semnată de ANAF.

Câmpuri Checkout B2B - Adaugă câmpurile CUI/CIF, Nr. Reg. Com., IBAN și Sector în pagina de finalizare a comenzii.

Mod Test - Suport pentru mediul Sandbox pentru testare înainte de punerea în funcțiune.

Compatibil HPOS - Funcționează cu sistemul High-Performance Order Storage din WooCommerce.

= Cum funcționează =
Configurezi datele companiei (CUI, Nume Firmă).

Înregistrezi aplicația pe portalul ANAF pentru a obține Client ID/Secret.

Conectezi plugin-ul la ANAF folosind certificatul digital.

Activezi modul Auto-Pilot sau generezi facturile manual din ecranul comenzii.

Plugin-ul se ocupă de generarea XML-ului, încărcare, verificarea statusului și descărcarea răspunsului.

= Cerințe =
WooCommerce 5.0 sau superior.

PHP 7.4 sau superior.

Cont activ în SPV (Spațiul Privat Virtual) ANAF.

Certificat digital calificat înregistrat la ANAF.

Aplicație înregistrată în Portalul Dezvoltatori ANAF.

= Documentație =
Pentru instrucțiuni detaliate de configurare, vă rugăm să consultați:

Ghid de Înregistrare ANAF OAuth

Ghid Tehnic RO e-Factura

= Suport =
Acest plugin este dezvoltat și întreținut de Creativ Digital Agency.

Pentru întrebări legate de suport, ne puteți contacta la: office@creativdigital.ro Răspundem tuturor solicitărilor în termen de 48 de ore în zilele lucrătoare.

== Instalare ==
Încarcă fișierele plugin-ului în /wp-content/plugins/e-factura-for-woocommerce/ sau instalează-l direct prin ecranul de module WordPress.

Activează plugin-ul prin secțiunea „Module” (Plugins) din WordPress.

Navighează la WooCommerce > RO e-Factura pentru configurare.

= Configurare Aplicație ANAF =
Mergi la Portalul ANAF > Dezvoltatori Aplicații > Adaugă aplicație.

Setează Redirect URI la: https://siteultau.ro/wp-admin/admin.php?page=wc-efactura-ro

Copiază valorile generate pentru Client ID și Client Secret.

Introdu aceste date în setările plugin-ului și apasă „Save”.

Apasă „Connect to ANAF” și autorizează conexiunea folosind certificatul digital.

== Întrebări Frecvente ==
= Am nevoie de un certificat digital? = Da. Autorizarea cu ANAF necesită un Certificat Digital Calificat (token) valid, înregistrat în contul tău SPV.

= Acest plugin este gratuit? = Da, acest plugin este complet gratuit și open-source. Se conectează direct la ANAF fără servicii terțe sau abonamente.

= Funcționează cu mediul de test ANAF? = Da. Activează „Test Mode (Sandbox)” în setări pentru a folosi API-ul de test ANAF înainte de a emite facturi reale.

= Ce format de factură generează? = Plugin-ul generează facturi XML UBL 2.1 conform standardului RO-CIUS solicitat de ANAF.

= Îl pot folosi pentru facturi B2C? = Plugin-ul este conceput în principal pentru facturarea B2B, conform legislației române. Facturile B2C pot fi generate, dar transmiterea lor către ANAF poate să nu fie obligatorie, în funcție de reglementările curente.

= Ce se întâmplă dacă ANAF respinge o factură? = Plugin-ul monitorizează statusul și adaugă note la comandă când o factură este validată sau respinsă. Dacă este respinsă, poți vedea eroarea, corecta datele și retrimite factura.

== Jurnal Modificări (Changelog) ==
= 1.0.2 =

S-a corectat „text domain” pentru a corespunde cu numele plugin-ului.

Îmbunătățiri pentru conformitatea cu Directorul de Module WordPress.org.

= 1.0.1 =

Consolidarea securității (verificare nonce, securizare output).

S-a adăugat trimiterea automată a facturii la finalizarea comenzii (Auto-Pilot).

Îmbunătățirea conformității PHPCS pentru standardele WordPress.org.

= 1.0.0 =

Lansare inițială.

Autentificare OAuth2 cu ANAF SPV.

Generare XML UBL 2.1.

Trimitere facturi manuală și automată.

Verificare status și descărcare ZIP.

== Politica de Confidențialitate ==
Acest plugin:

Stochează token-urile OAuth securizat în baza de date WordPress.

Trimite datele facturii direct către ANAF (nu către servere terțe).

Nu colectează și nu transmite date către dezvoltatorii plugin-ului.

Stochează fișierele XML generate și răspunsurile ANAF în folderul wp-content/uploads.






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
