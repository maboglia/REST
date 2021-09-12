# MIME

MIME "Multipurpose internet mail extensions" è uno standard per descrivere i documenti in altre forme oltre al testo ASCII, ad es. audio, video e immagini. Inizialmente utilizzato per gli allegati di posta elettronica, è diventato lo standard di fatto per definire i tipi di documenti ovunque.

---

## Tipo MIME

Un tipo MIME (ora chiamato propriamente "tipo di media", ma a volte anche "tipo di contenuto") è una stringa inviata insieme a un file che indica il tipo di file (che descrive il formato del contenuto, ad esempio, un file audio potrebbe essere etichettato come audio/ogg o un file immagine image/png).

Ha lo stesso scopo delle estensioni dei nomi di file tradizionalmente su Windows. Il nome deriva dallo standard MIME originariamente utilizzato nella posta elettronica.

---

## Tipi MIME comuni

Di seguito è riportato un elenco di tipi MIME, associati per tipo di documenti, ordinati in base alle loro estensioni comuni.

Due tipi MIME primari sono importanti per il ruolo dei tipi predefiniti:

* `text/plain` è il valore predefinito per i file di testo. Un file di testo deve essere leggibile dall'uomo e non deve contenere dati binari.
* `application/octet-stream` è il valore predefinito per tutti gli altri casi. Un tipo di file sconosciuto dovrebbe utilizzare questo tipo. I browser prestano particolare attenzione quando manipolano questi file, cercando di salvaguardare l'utente per prevenire comportamenti pericolosi.

---

IANA è il registro ufficiale dei tipi di media MIME e mantiene un elenco di tutti i tipi MIME ufficiali. Questa tabella elenca alcuni importanti tipi MIME per il Web:

Estensione Tipo di documento Tipo MIME
* **.aac** AAC audio audio/aac
* **.abw** Applicazione per documenti AbiWord/x-abiword
* **.arc** Archivio documento (più file incorporati) application/x-freearc
* **.avi** AVI: Audio Video Interleave video/x-msvideo
* **.azw** Applicazione formato eBook Amazon Kindle/vnd.amazon.ebook
* **.bin** Qualsiasi tipo di application/octet-stream di dati binari
* **.bmp** Windows OS/2 immagine grafica bitmap/bmp
* **.bz** Applicazione archivio BZip/x-bzip
* **.bz2** Applicazione archivio BZip2/x-bzip2
* **.csh** Applicazione script C-Shell/x-csh
* **.css** Cascading Style Sheets (CSS) text/css
* **.csv** Valori separati da virgole (CSV) text/csv


---


* **.doc** Applicazione Microsoft Word/msword
* **.docx** Applicazione Microsoft Word (OpenXML)/vnd.openxmlformats-officedocument.wordprocessingml.document
* **.eot** MS Embedded OpenType fonts application/vnd.ms-fontobject
* **.epub** Applicazione di pubblicazione elettronica (EPUB)/epub + zip
* **.gz** Applicazione archivio compresso GZip/gzip
* **.gif** Immagine/gif Graphics Interchange Format (GIF)
* **.htm**
* **.html** HTML (HyperText Markup Language) text/html
* **.ico** Icon format image/vnd.microsoft.icon
* **.ics** Testo/calendario in formato iCalendar
* **.jar** Applicazione JAR (Java Archive)/java-archive
* **.jpeg**
* **.jpg** Immagini JPEG image/jpeg
* **.js** JavaScript

text/javascript, secondo le seguenti specifiche:

* https://html.spec.whatwg.org/multipage/#scriptingLanguages
* https://html.spec.whatwg.org/multipage/#dependencies:willful-violation
* https://datatracker.ietf.org/doc/draft-ietf-dispatch-javascript-mjs/

---

* **.json** Formato JSON application/json
* **.jsonld** Applicazione in formato JSON-LD/ld + json
* **.mid**
* **.midi** MIDI (Musical Instrument Digital Interface) audio/midi audio/x-midi
* **.mjs** JavaScript modulo testo/javascript
* **.mp3** Audio audio MP3/mpeg
* **.cda** Applicazione CD audio/x-cdf
* **.mp4** MP4 audio video/mp4
* **.mpeg** MPEG Video video/mpeg
* **.mpkg** Pacchetto di installazione Apple application/vnd.apple.installer + xml
* **.odp** Documento di presentazione OpenDocument application/vnd.oasis.opendocument.presentation
* **.ods** OpenDocument documento del foglio di calcolo application/vnd.oasis.opendocument.spreadsheet
* **.odt** Documento di testo OpenDocument application/vnd.oasis.opendocument.text

---

* **.oga** OGG audio audio/ogg
* **.ogv** OGG video video/ogg
* **.ogx** OGG application/ogg
* **.opus** Opus audio audio/opus
* **.otf** OpenType font font/otf
* **.png** Portable Network Graphics immagine/png
* **.pdf** Applicazione/pdf Adobe Portable Document Format (PDF)
* **.php** Hypertext Preprocessor (home page personale) application/x-httpd-php
* **.ppt** Applicazione Microsoft PowerPoint/vnd.ms-powerpoint
* **.pptx** Applicazione Microsoft PowerPoint (OpenXML)/vnd.openxmlformats-officedocument.presentationml.presentation
* **.rar** Applicazione archivio RAR/vnd.rar
* **.rtf** Rich Text Format (RTF) applicazione/rtf
* **.sh** Applicazione script di shell Bourne/x-sh
* **.svg** Immagine SVG (Scalable Vector Graphics)/svg + xml
* **.swf** Piccolo formato web (SWF) o applicazione per documenti Adobe Flas  x-shockwave-flash

---

Applicazione 

* **.tar** Tape Archive (TAR)/x-tar
* **.tif**
* **.tiff** TIFF (Tagged Image File Format) image/tiff
* **.ts** MPEG Transport Stream video/mp2t
* **.ttf** Carattere TrueType font/ttf
* **.txt** Testo, (generalmente ASCII o ISO 8859-n) text/plain
* **.vsd** Applicazione Microsoft Visio/vnd.visio
* **.wav** Forma d'onda Formato audio audio/wav
* **.weba** WEBM audio audio/webm
* **.webm** WEBM video video/webm
* **.webp** WEBP immagine immagine/webp

---

* **.woff** Web Open Font Format (WOFF) font/woff
* **.woff2** Web Open Font Format (WOFF) font/woff2
* **.xhtml** Applicazione XHTML/xhtml + xml
* **.xls** Applicazione Microsoft Excel/vnd.ms-excel
* **.xlsx** Applicazione Microsoft Excel (OpenXML)/vnd.openxmlformats-officedocument.spreadsheetml.sheet
* **.xml** XML application/xml se non leggibile da utenti occasionali (RFC 3023, sezione 3)
* **text/xml** se leggibile da utenti occasionali (RFC 3023, sezione 3)
* **.xul** applicazione XUL/vnd.mozilla.xul + xml
* **.zip** applicazione di archivio ZIP/zip
* **.3gp** 3GPP contenitore audio/video video/3gpp
* **audio/3gpp** se non contiene video
* **.3g2** 3GPP2 contenitore audio/video video/3gpp2
* **audio/3gpp2** se non contiene video
* **.7z** Applicazione di archivio 7-zip/x-7z-compresso