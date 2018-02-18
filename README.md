# HEAD

[![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Contributors](https://img.shields.io/github/contributors/joshbuchea/head.svg)](https://github.com/joshbuchea/HEAD/graphs/contributors)

Alles was in den Kopf-Bereich einer HTML-Datei kommen kann. 
Dies ist die deutsche Übersetzung von https://github.com/joshbuchea

## Inhaltsverzeichnis

- [Empfohlenes Minimum](#empfohlenes-minimum)
- [Elemente](#elemente)
- [Meta](#meta)
- [Link](#link)
- [Icons](#icons)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter Card](#twitter-card)
  - [Twitter Privacy](#twitter-privacy)
  - [Google+ / Schema.org](#google--schemaorg)
  - [Pinterest](#pinterest)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [OEmbed](#oembed)
- [Browsers / Platforms](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Browsers (Chinese)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App Links](#app-links)
- [Weitere Ressourcen](#weitere-resources)
- [Verwandte Projekte](#verwandte-projekte)
- [Andere Formate](#andere-formate)
- [Übersetzungen](#übersetzungen)
- [Beitragen](#Beitragen)
  - [Beitragende](#beitragende)
- [Autor](#autor)
- [Lizens](#lizens)

## Empfohlenes Minimum

Unten sind die essentiellen Elemente eines jeden Webdokumentes (Webseiten/Apps):

```html
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge"> <!-- † -->
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<!--
  Diese 3 Meta-Tags *müssen* in jedem <head>-Element als erstes stehen, 
  um sicherzustellen, dass das Dokument richtig dargestellt wird.
  Alle anderen Elemente im <head>-Element sollten *nach* diesen Tags stehen.

  † Man benutzt den content="ie-edge" Tag, wenn das Projekt 
    Internet Explorer vor Version 11 unterstützt.
 -->
<title>Seiten Titel</title>
```

**[⬆ nach oben](#inhaltsverzeichnis)**

## Elemente

Gültige `<head>` Elemente schließen `meta`, `link`, `title`, `style`, `script`, `noscript`, und `base` ein.

Diese Elemente stellen Informationen bereit, wie das Dokument von den verschiedensten Webtechnologien aufgenommen und dargestellt werden soll, z.B. von Browsern, Suchmaschinen, Robotern, usw.

```html
<!--
  Legt die Zeichenkodierung für dieses Dokument fest, so 
  das alle Zeichen innerhalb UTF-8 (zum Beispiel Umlaute)
  richtig dargestellt werden.
-->
<meta charset="utf-8">

<!-- Legt den Titel des Dokumentes fest -->
<title>Page Title</title>

<!-- Legt die Basis URL für alle relativen URLs 
  innerhalb des Dokumentes fest -->
<base href="http://example.com/page.html">

<!-- Verlinkt zu einem externen CSS-Dokument -->
<link rel="stylesheet" href="styles.css">

<!-- Für CSS innerhalb des Dokumentes -->
<style>
  /* ... */
</style>

<!-- JavaScript & No-JavaScript Tags -->
<script src="script.js"></script>
<script>
  // function(s) go here
</script>
<noscript>
  <!-- Kein JS - Alternative -->
</noscript>
```

**[⬆ nach oben](#inhaltsverzeichnis)**

## Meta

```html
<!--
  Diese 3 Meta-Tags *müssen* in jedem <head>-Element als erstes stehen, 
  um sicherzustellen, dass das Dokument richtig dargestellt wird.
  Alle anderen Elemente im <head>-Element sollten *nach* diesen Tags stehen.
-->
<meta charset="utf-8">
<meta http-equiv="x-ua-compatible" content="ie=edge">
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

<!--
  Erlaubt die Kontrolle, von wo Ressourcen geladen werden.
  Sollte so weit obend wie möglich im <head> platziert werden, da 
  nur die Ressourcen nach diesem Tag berücksichtigt werden.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Name der Web Applikation (sollte nur genutzt werden, wenn die Webseite wie eine App genutzt wird) -->
<meta name="application-name" content="Application Name">

<!-- Hauptfarbe für Chrome, Firefox OS und Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Eine kurze Beschreibung des Dokuments (max. 150 Zeichen)
     Diese wird möglicherweise in Suchmaschinen angezeigt. -->
<meta name="description" content="Eine Beschreibung der Webseite">

<!-- Kontrolliert das Verhalten von Suchmaschinen-Crawlern und Indexierung der Seite -->
<meta name="robots" content="index,follow"><!-- Alle Suchmaschinen -->
<meta name="googlebot" content="index,follow"><!-- Speziell an Google -->

<!-- Sagt Google, dass in der Suche keine Sitelinks-Suchbox auftauchen soll -->
<meta name="google" content="nositelinkssearchbox">

<!-- Sagt Google, dass es keine Übersetzung für das Dokument bereitstellen soll -->
<meta name="google" content="notranslate">

<!-- Verifikation des Besitzers der Webseite -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Identifiziert die Software, mit der das Dokument erstellt wurde (z.B. WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Kurze Beschreibung des Themas des Dokumentes -->
<meta name="subject" content="your document's subject">

<!-- Gibt eine Altersfreigabe für das Dokument an -->
<meta name="rating" content="General">

<!-- Erlaubt die Kontrolle darüber, wie Referrer Information weitergeleitet wird -->
<meta name="referrer" content="no-referrer">

<!-- Keine automatische Erkennung und Formattierung von Telefonnummern erlauben -->
<meta name="format-detection" content="telephone=no">

<!-- Kein DNS Prefetching erlauben -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Speichert ein Cookie im Webbrowser des Benutzers, um diesen identifizieren zu können -->
<meta http-equiv="set-cookie" content="name=value; expires=date; path=url">

<!-- Gibt an, in welchem speziellen Frame das Dokument erscheinen soll -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo-Tags -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Ländercode (ISO 3166-1): obligatorisch, Code des US-Staates (ISO 3166-2): optional; z.B. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- z.B. content="New York City" -->
```

- 📖 [Meta-Tags, die Google versteht](https://support.google.com/webmasters/answer/79812?hl=de)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions) (auf Englisch)
- 📖 [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use) (auf Englisch)
- 📖 [Geotagging on Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Link

```html
<!-- Verlinkt ein externes Stylesheet -->
<link rel="stylesheet" href="http://example.com/styles.css">

<!-- Verhindert Probleme mit verdoppelten Inhalten -->
<link rel="canonical" href="http://example.com/article/?page=2">

<!-- Verlinkt zu einer AMP HTML Version des aktuellen Dokumentes -->
<link rel="amphtml" href="http://example.com/path/to/amp-version.html">

<!-- Verlinkt zu einer JSON-Datei, welche Installations Daten für eine WebApp bereitstellt -->
<link rel="manifest" href="manifest.json">

<!-- Verlinkt zu Informationen über den/die Autor(en) des Dokumentes -->
<link rel="author" href="humans.txt">

<!-- Referriert zu einem Statement zum Urheberrecht im Zusammenhang mit dem angegebenen Link -->
<link rel="license" href="copyright.html">

<!-- Gibt eine Referenz zu einem Bereich im Dokument, welcher eine andere Sprache benutzt -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Gibt Informationen über den Autor oder eine andere Person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Verlinkt zu einem Dokument, welches Aufzeichnungen, Dokumente oder andere Materialien von historischem Interesse enthält -->
<link rel="archives" href="http://example.com/archives/">

<!-- Verlinkt zu einer Top Level Ressource in einer hierarchischen Struktur -->
<link rel="index" href="http://example.com/article/">

<!-- Stellt eine Referenz auf sich selbst zur Verfügung - sinnvoll wenn ein Dokument mehrere mögliche Referenzen hat -->
<link rel="self" type="application/atom+xml" href="http://example.com/atom.xml">

<!-- Das erste, letzte, vorherige und nächste Dokument in einer Serie von Dokumenten -->
<link rel="first" href="http://example.com/article/">
<link rel="last" href="http://example.com/article/?page=42">
<link rel="prev" href="http://example.com/article/?page=1">
<link rel="next" href="http://example.com/article/?page=3">

<!-- Wird genutzt, wenn ein Blog von einer dritten Partei bereitgestellt wird. -->
<link rel="EditURI" href="http://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Formuliert einen automatischen Kommentar, wenn ein anderer WordPress Blog auf den eigenen WordPress Blog verlinkt -->
<link rel="pingback" href="http://example.com/xmlrpc.php">

<!-- Informiert eine URL, wenn in diesem Dokument auf diese verlinkt wird -->
<link rel="webmention" href="http://example.com/webmention">

<!-- Erlaubt das Posten an die eigene Domain mit einem Mircopub Client -->
<link rel="micropub" href="http://example.com/micropub">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="http://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="http://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Icons

```html
<!-- Für IE 10 und älter -->
<!-- Platziere favicon.ico in dem Root Ordner - keine Tags notwendig -->

<!-- Icon in der höchsten Auflösung, die gebraucht wird -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Safari Pinned Tab Icon -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/) (auf Englisch)
- 📖 [Creating Pinned Tab Icons](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html) (auf Englisch)
- 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet) (auf Englisch)
- 📖 [Icons & Browser Colors](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Social

### Facebook Open Graph

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="http://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Titel der Webseite">
<meta property="og:image" content="http://example.com/image.jpg">
<meta property="og:description" content="Beschreibung der Webseite">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)
- 📖 [Open Graph protocol](http://ogp.me/) (auf Englisch)
- 🛠 Test your page with the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) (auf Englisch)

### Twitter Card

```html
<meta name="twitter:card" content="Zuammenfassung">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="http://example.com/page.html">
<meta name="twitter:title" content="Titel der Webseite">
<meta name="twitter:description" content="Beschreibung der Seite in weniger als 200 Zeichen">
<meta name="twitter:image" content="http://example.com/image.jpg">
```

- 📖 [Getting started with cards — Twitter Developers](https://dev.twitter.com/cards/getting-started) (auf Englisch)
- 🛠 Test your page with the [Twitter Card Validator](https://cards-dev.twitter.com/validator) (auf Englisch)

### Twitter Privatsphäre
Wenn Tweets in die Webseite eingebunden werden, dann kann Twitter Informationen von der Webseite nutzen, um  Twitter Nutzern passende Inhalte anzuzeigen. [Mehr über Twitters Privatsphäre Einstellungen](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- verbietet Twitter die Nutzung der Inhalte der Webseite für Personalisierungszwecke -->
<meta name="twitter:dnt" content="on">
```

### Google+ / Schema.org

```html
<html lang="" itemscope itemtype="http://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Titel der Seite">
      <meta itemprop="description" content="Beschreibung der Seite in weniger als 200 Zeichen">
      <meta itemprop="image" content="http://example.com/image.jpg">
```

**Hinweis:** Dieses Markup verlangt Attribute im ersten html-Tag

- 🛠 Testen Sie die Webseite mit dem [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/) (auf Englisch)

### Pinterest

Pinterest hilft zu verhindern, das Leute Dinge von der Webseite speichern können. [Pinterests Hilfecenter](https://help.pinterest.com/en/articles/prevent-people-saving-things-pinterest-your-site). Die `description` ist optional.

```html
<meta name="pinterest" content="nopin" description="Du kannst nicht von dieser Webseite speichern!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- Die URL der Webversion des entsprechenden Artikels -->
<link rel="canonical" href="http://example.com/article.html">

<!-- Der Style der für diesen Artikel genutzt werden soll -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Creating Articles - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate) (auf Englisch)
- 📖 [Code Samples - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference) (auf Englisch)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="http://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [oEmbed format](http://oembed.com/) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Browsers / Platforms

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Verhindert die automatische Erkennung und Formattierung von Telefonnummern -->
<meta name="format-detection" content="telephone=no">

<!-- Start Icon (180x180px oder größer) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Start Screen Bild -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Start Icon Titel -->
<meta name="apple-mobile-web-app-title" content="App Titel">

<!-- Erlaubt Standalone (full-screen) Modus -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Aussehen der Statusbar (hat keinen Effekt, wenn nicht Standalone Modus aktiv ist) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html) (auf Englisch)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Dem Startbildschirm hinzufügen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Mehr Infos: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Verhindert Übersetzung -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Zwingt IE 8/9/10 die neueste Rendering Engine zu nutzen -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Verhindert die automatische Erkennung und Formattierung von Telefonnummern durch die Skype Toolbar Browser Erweiterung -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- IE10: Verhindert das Hervorheben von Links durch Berührung (https://blogs.windows.com/buildingapps/2012/11/15/adapting-your-webkit-optimized-site-for-internet-explorer-10/) -->
<meta name="msapplication-tap-highlight" content="no">

<!-- Gepinnte Seiten (https://msdn.microsoft.com/en-us/library/dn255024(v=vs.85).aspx) -->
<meta name="application-name" content="Beispiel Titel">
<meta name="msapplication-tooltip" content="Eine Beschreibung darüber, was die Seite tut.">
<meta name="msapplication-starturl" content="http://example.com/index.html?pinned=true">
<meta name="msapplication-navbutton-color" content="#FF3300">
<meta name="msapplication-window" content="width=800;height=600">
<meta name="msapplication-task" content="name=Task 1;action-uri=http://host/Page1.html;icon-uri=http://host/icon1.ico">
<meta name="msapplication-task" content="name=Task 2;action-uri=http://microsoft.com/Page2.html;icon-uri=http://host/icon2.ico">
<meta name="msapplication-badge" value="frequency=NUMBER_IN_MINUTES;polling-uri=http://example.com/path/to/file.xml">
<meta name="msapplication-TileColor" content="#FF3300">
<meta name="msapplication-TileImage" content="/path/to/tileimage.jpg">

<meta name="msapplication-config" content="http://example.com/browserconfig.xml">
<meta name="msapplication-notification" content="frequency=60;polling-uri=http://example.com/livetile;polling-uri2=http://example.com/livetile2">
<meta name="msapplication-task-separator" content="1">
```

**[⬆ nach oben](#inhaltsverzeichnis)**

## Browser (Chinese)

### 360 Browser

```html
<!-- Wählt die Reihenfolge der Rendering Engines -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Hält den Bildschirm in einer bestimmten Orientierung -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Zeigt das Dokument im Vollbildmodus -->
<meta name="x5-fullscreen" content="true">

<!-- Zeigt das Dokument im "application mode" (Vollbild, usw.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Hält den Bildschirm in einer bestimmten Orientierung -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Zeigt das Dokument im Vollbildmodus -->
<meta name="full-screen" content="yes">

<!-- UC Browser zeigt Bilder auch dann an, wenn in "text mode" -->
<meta name="imagemode" content="force">

<!-- Zeigt das Dokument im "application mode" (Vollbild, verbotene Bewegungen, usw.) -->
<meta name="browsermode" content="application">

<!-- Verhindert den "Nachtmodus" des UC Browsers für dieses Dokument -->
<meta name="nightmode" content="disable">

<!-- Vereinfacht das Dokument, um Datentransfer zu reduzieren -->
<meta name="layoutmode" content="fitscreen">

<!-- Verhindert im UC Browser das Vergößern der Schrift, wenn viele Wörter im Dokument sind -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](http://www.uc.cn/download/UCBrowser_U3_API.doc) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## App Links

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="http://applinks.org/documentation">
```

- 📖 [App Links](http://applinks.org/documentation/) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Weitere Ressourcen

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md) (auf Englisch)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Verwandte Projekte

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package für `HEAD` Snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package für `HEAD` Snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface für `HEAD` Snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulieren der Meta Information in dem `HEAD` Tag mit Vue.js

**[⬆ nach oben](#inhaltsverzeichnis)**

## Andere Formate

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md) (auf Englisch)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Übersetzungen

- 🇧🇷 [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- 🇮🇹 [Italian](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanese](http://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Korean](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russian/Русский](https://github.com/Konfuze/HEAD)
- 🇹🇷 [Turkish/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ nach oben](#inhaltsverzeichnis)**

## Beitragen

Öffne ein *Issue*, um auf Verbesserungen oder Änderungen hinzuweisen oder mache ein *Pull Request*, um selber diesem Dokument etwas hinzuzufügen.

### Beitragende

Hier sind alle Beitragende zu diesem Dokument zu sehen [contributors](https://github.com/Shidigital/HEAD/graphs/contributors).

## Autor

**[Josh Buchea](https://joshbuchea.com/)**

## Übersetzerin

**[Shidigital](https://github.com/Shidigital)**

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ nach oben](#inhaltsverzeichnis)**
