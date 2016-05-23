##  Userscript Manager

<small>För att få upp lite tempo i utvecklingen sitter vi med en lokal _webbserver_ och en _userscript manager_ som vi exekverar koden ifrån (istället för att ladda upp det i AB-testningsverktyget).</small>

####1.
- Firefox: Greasemonkey
- Chrome: Tampermonkey

####2.
ladda ner här: <b>http://dah.la/1Kd8cEX</b>

<pre><code class="javascript">
// ==UserScript==
// @name        AB injection Script
// @author       Conversionista!
// @namespace    optcli
// @description  Inject local experiment JS / CSS into a Chrome page for development 
// @include      /ab=true/
// @require      http://ajax.googleapis.com/ajax/libs/jquery/1.6.4/jquery.js
// ==/UserScript==

var scriptElement = document.createElement('script');
scriptElement.type = 'text/javascript';
scriptElement.src =  'http://localhost:8080/variation.js';
document.head.appendChild(scriptElement);

var stylesheet = document.createElement('link');
stylesheet.rel = 'stylesheet';
stylesheet.href = 'http://localhost:8080/variation.css';
document.head.appendChild(stylesheet);
</code></pre>