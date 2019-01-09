# canada-divorces-analysis
inline-HTML

<head><meta charset="utf-8" />
<title>Divorces in Canada, Data Analysis</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}

@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Divorces-in-Canada,-Data-Analysis">Divorces in Canada, Data Analysis<a class="anchor-link" href="#Divorces-in-Canada,-Data-Analysis">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Jeremy Friesen, 100649797, 2018-12-10</p>
<p>In this notebook, we'll be analyzing data from the <a href="https://open.canada.ca/data/en/dataset?portal_type=dataset">Canada Open Data Portal</a> about divorces in Canada. We'll be using the numpy, pandas and matplotlib libraries to help with the analysis. The datasets used (and their sizes) are as follows:</p>
<ul>
<li><a href="https://open.canada.ca/data/en/dataset/0966ab3e-15c3-4e57-bfb2-5161a259386b">Divorce rates, by year of marriage</a> (650, 14)</li>
<li><a href="https://open.canada.ca/data/en/dataset/c5827d4a-9820-4b0b-b2ae-ca5f02269089">Divorces, by duration of marriage</a> (1204, 15)</li>
<li><a href="https://open.canada.ca/data/en/dataset/f869cd9e-c9dd-474c-b967-8363d3ca6062">Divorces, by reason for marital breakdown</a> (140, 15)</li>
<li><a href="https://open.canada.ca/data/en/dataset/d6e56d93-d513-44f4-91d0-d35d639e9ae3">Vital statistics, divorces</a> (446, 15)</li>
<li><a href="https://open.canada.ca/data/en/dataset/23fcb096-3926-49ff-9214-0dca15d8c035">Estimates of population, by marital status, age group and sex for July 1, Canada, provinces and territories</a> (1070880, 18)</li>
</ul>
<p>These data sources are interesting and relevant because divorces can say a lot about our society. Divorces are the legal termination of marriage, and statistics about them can describe the breakdown of long term relationships.</p>
<p>Let's start by importing the necessary packages:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">pl</span>
<span class="kn">from</span> <span class="nn">matplotlib.legend_handler</span> <span class="k">import</span> <span class="n">HandlerLine2D</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Divorce-Rates-by-Year-of-Marriage">Divorce Rates by Year of Marriage<a class="anchor-link" href="#Divorce-Rates-by-Year-of-Marriage">&#182;</a></h2><p>As a starting point, let's look at divorce rates by the year the couples were married.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[114]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">divorceRatesByYearOfMarriage</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;divorceRatesByYearOfMarriage.csv&#39;</span><span class="p">)</span>
<span class="c1"># print the size of the dataset</span>
<span class="nb">print</span><span class="p">(</span><span class="n">divorceRatesByYearOfMarriage</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>

<span class="c1"># Trim the &quot;, place of occurence&quot; substring from the GEO column</span>
<span class="n">divorceRatesByYearOfMarriage</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorceRatesByYearOfMarriage</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>

<span class="c1"># Set the index to the year of marriage</span>
<span class="n">divorceRatesByYearOfMarriage</span> <span class="o">=</span> <span class="n">divorceRatesByYearOfMarriage</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s1">&#39;Year of marriage&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">sort_index</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>(650, 15)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Graph each province/territory&#39;s Divorce Rates by Year of Marriage</span>
<span class="n">GEOs</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Canada&#39;</span><span class="p">,</span> <span class="s1">&#39;Newfoundland and Labrador&#39;</span><span class="p">,</span> <span class="s1">&#39;Prince Edward Island&#39;</span><span class="p">,</span> <span class="s1">&#39;Nova Scotia&#39;</span><span class="p">,</span> <span class="s1">&#39;New Brunswick&#39;</span><span class="p">,</span> <span class="s1">&#39;Quebec&#39;</span><span class="p">,</span> <span class="s1">&#39;Ontario&#39;</span><span class="p">,</span>
        <span class="s1">&#39;Manitoba&#39;</span><span class="p">,</span> <span class="s1">&#39;Saskatchewan&#39;</span><span class="p">,</span> <span class="s1">&#39;Alberta&#39;</span><span class="p">,</span> <span class="s1">&#39;British Columbia&#39;</span><span class="p">,</span> <span class="s1">&#39;Yukon&#39;</span><span class="p">,</span> <span class="s1">&#39;Northwest Territories and Nunavut&#39;</span><span class="p">]</span>
<span class="n">colors</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;yellow&#39;</span><span class="p">,</span> <span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="s1">&#39;purple&#39;</span><span class="p">,</span> <span class="s1">&#39;green&#39;</span><span class="p">,</span> <span class="s1">&#39;brown&#39;</span><span class="p">,</span> <span class="s1">&#39;pink&#39;</span><span class="p">,</span> <span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="s1">&#39;black&#39;</span><span class="p">,</span> <span class="s1">&#39;cyan&#39;</span><span class="p">,</span> <span class="s1">&#39;magenta&#39;</span><span class="p">,</span> <span class="s1">&#39;gray&#39;</span><span class="p">,</span> 
           <span class="s1">&#39;maroon&#39;</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">GEOs</span><span class="p">)):</span>
    <span class="n">pl</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">divorceRatesByYearOfMarriage</span><span class="p">[</span><span class="n">divorceRatesByYearOfMarriage</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">GEOs</span><span class="p">[</span><span class="n">i</span><span class="p">]][</span><span class="s1">&#39;VALUE&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="n">colors</span><span class="p">[</span><span class="n">i</span><span class="p">]);</span>
    
<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Divorce Rates by Year of Marriage, Canada 1955-2004&quot;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">GEOs</span><span class="p">,</span> <span class="n">loc</span><span class="o">=</span><span class="s1">&#39;center left&#39;</span><span class="p">,</span> <span class="n">bbox_to_anchor</span><span class="o">=</span><span class="p">(</span><span class="mf">1.0</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">))</span>
<span class="n">pl</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Year&quot;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Rate per 1,000 Marriages&quot;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Graph-Analysis">Graph Analysis<a class="anchor-link" href="#Graph-Analysis">&#182;</a></h2><p>There seems to be a significant upwards trend on the graphs for each province/territory and Canada as a whole. There's a few 0's in the data as well, which likely just means the data for those years is unreported.</p>
<p>The data seems to peak at around 2000. Since this data was published in 2004, couples married since 2000 would have been married less than 4 years, and possibly less likely to get divorced because of the short span of time they have been married.</p>
<p>To test this, let's analyze data which reports divorce rates by length of marriage.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[113]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">divorcesByDurationOfMarriage</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;divorcesByDurationOfMarriage.csv&#39;</span><span class="p">)</span>
<span class="c1"># print the size of the dataset</span>
<span class="nb">print</span><span class="p">(</span><span class="n">divorcesByDurationOfMarriage</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>

<span class="n">divorcesByDOM</span> <span class="o">=</span> <span class="n">divorcesByDurationOfMarriage</span>

<span class="c1"># Trim the &quot;, place of occurrence&quot; substring from the &#39;GEO&#39; column</span>
<span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorcesByDurationOfMarriage</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>

<span class="c1"># Trim the &quot;Duration of marriage,&quot; substring from the &#39;Duration of marriage&#39; column</span>
<span class="n">divorcesByDOM</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span> <span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span>

<span class="c1"># Filters data so that the &#39;Duration of marriage&#39; column will only have exct year values</span>
<span class="n">divorcesByDOM</span> <span class="o">=</span> <span class="n">divorcesByDOM</span><span class="p">[(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;to&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;all years&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;not stated&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;and over&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>(1204, 15)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="The-graph-for-divorces-by-duration-of-marriage-for-all-of-Canada(2005)-looks-like-this:">The graph for divorces by duration of marriage for all of Canada(2005) looks like this:<a class="anchor-link" href="#The-graph-for-divorces-by-duration-of-marriage-for-all-of-Canada(2005)-looks-like-this:">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">canadaDivorcesByDOM</span> <span class="o">=</span> <span class="n">divorcesByDOM</span><span class="p">[(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">divorcesByDOM</span><span class="p">[</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="mi">2005</span><span class="p">)]</span>
<span class="n">xs</span> <span class="o">=</span> <span class="n">canadaDivorcesByDOM</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">ys</span> <span class="o">=</span> <span class="n">canadaDivorcesByDOM</span><span class="p">[</span><span class="s1">&#39;VALUE&#39;</span><span class="p">]</span>
<span class="n">pl</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">xs</span><span class="p">,</span> <span class="n">ys</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">);</span>

<span class="n">pl</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration of Marriage before Divorce&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of divorces&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Number of Divorces vs Duration of Marriage, Canada 2005&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAZUAAAEWCAYAAACufwpNAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAIABJREFUeJzt3XecVNX9//HXm6KggIIioqBYUAMaMa6IHTvRWOLPGE2M
GluMxvJNscSGGmsSNcZoosaIDVvssUTBHhEXBQQUQQFhRcAWsKHA5/fH50wYx9nd2WVmZ2b5PB+P
ecydc8ucO3dmPveec885MjNCCCGEYmhT7gyEEEJoPSKohBBCKJoIKiGEEIomgkoIIYSiiaASQgih
aCKohBBCKJoIKgWQdJOk35XpvSXpH5I+kjS6mdtYR9InktoWO3+haSQ9KunwMrzv7yS9L+m9ln7v
PHn5raQbyp2PSiLpaUlHlzsfxVCVQUXSdElzJa2clXa0pKfLmK1S2R7YHehlZgNzZ0o6QtLiFDQ+
kTQtBaGNMsuY2Ttm1snMFrdkxitJ+s58LmmBpI8l/UfScZJK9huQNFTSrdlpZvZdMxtWqvesJx/r
AL8C+pnZmnnmD5Zkku7LSd88pT9dzPyY2UVmVvY/0HTCdpKkCZI+lTRL0t2SNit33golaQ1JwyW9
K+m/kl6QtHXOMj+SNCPt4/2SumXNW1HSjZLmS3pP0i9z1rW0Xub/pdGTgaoMKklb4ORyZ6KpmnG1
sC4w3cw+bWCZF82sE7AKsBvwOTBG0qbNzGZBJLUr5fZLYB8z64x/ppcApwF/b86Gqmzf1wE+MLO5
DSwzD9hG0mpZaYcDbzb3TfN9RhX2uf0J/w85CegGbATcD+xdzkw1USfgZWBLfB+GAf+S1AlAUn/g
b8BPgB7AZ8A1WesPBfriv4mdgVMlDcl5j83TSWmngk4GzKzqHsB04HTgQ2DVlHY08HSa7gMY0C5r
naeBo9P0EcALwBXAx8DbwLYpfSYwFzg8a92bgL8CTwALgGeAdbPmb5LmfQhMBg7KWfda4BHgU2C3
PPuzFvBgWn8qcExKPwr4AlgMfAKcl2fdI4Dn86Q/DNyT+3kAPwRqc5b9P+DBNL0KcDP+JzMDOAto
k+dz+wD4XUo/Bng9fTaTgO9k7dc/07amASdlvedAoBaYD8wBLq/nWL8OfC/rdbu0ve8AHYBbU14+
xn9cPRr4zuyWkzYQWAJsmvsdyffZps/wBGAKMC2l/Sl9Z+YDY4AdUvoQ4Evgq3TsxuX5HrZJn+8M
/Dt3M7BKzjE7HHgHeB84s4HfRN7jxtKTjCUpHzflWXcwMAv/jp+Q0toCdcA5pN9VQ/ub5g0F7knH
ZD7+m6wv7das9e4G3gP+CzwL9M+atxrwUFr3ZeB3Ocek3t9eI/8hffHf1cAGltkbeDW990xgaNa8
Bo8P/t16Ef9ezgauBlbImr878Eba56vx/5TM92IDYCT+vX4fuI30P1fgvs0HtkzTFwG3Z83bAP9e
dk6v3wX2yJp/PnBHznd+w0Lf28yqOqjsBtzL0j+2pgaVRcBP04/nd+mL8RdgRWAP/A+yU1r+pvR6
xzT/T5kvNrBy+sL9FP/D2yJ9EfplrftfYDv8R94hz/48i589dAAG4H8Mu2Tl9RtBI2vdvPOBI4E5
uZ8HsFLal75Zy74MHJymbwYeADqn9d4Ejsr53E5M2+oI/AD/89kKELAhftbTBv/TOQdYAVgfD957
pm29CPwkTXcCBtWzf+cAt+X80F9P0z/D/3BWSsdxS6BLQ9+ZPOnvAD/P/Y7k+2zTZ/gEfkbYMaUd
iv/xtcOLmN7LHGNy/jzzfA+PxE8i1k+fwb3ALTnH7Pr0OW8OLAS+Vc/+NXTcBgOzGvgODcaDyrbA
SyltL+Bxsn5XBe7vV8D+6fh3bCAtO6gcmfK9InAlMDZr3h3psRLQD/+tFfTba+Q/5DhgRiPLDAY2
S/n+Nn7ys38hxwf/Lg5K+eqDnxydkuatjv8GDwTa4yd1i7K+FxviQWdFoDv+/3Blgf+NA/AT0czJ
yQPAaTnLLEj565r2oUfWvP8HvJbznX83Hed7gT6N5qGQjFbag6VBZVP8D7s7TQ8qU7LmbZbnw/0A
GJCmb+Lr0bsTfpbTGz/zfy4nf38Dzs1a9+YG9qV32lbnrLSLSWeUND+oDAG+yvd54GeN56TpvulL
lvlj/pKsHyX+x/101nu9k/M+jwMn53n/rfMsewbwjzT9LHAesHojx3rDTP7S69uy8n4k8B/g24V+
Z/KkjyKdYVJYUNmlkff5CC8ugMaDygjg+Kx5G+N/wJk/IsPr0jLzR5OCf842GztugykgqKTpKSkf
dwA/JieoFLC/z+bMry/t1nq2t2ra71XSfn0FbJw1/39XKjTy22vkOJ0JjGpsuZx1rgSuyPlNNXp8
0rxTgPvS9GHZ742fjM3K/u7lrLs/8GoB+esCvAackZU2AjguZ7m6dMx7p33okDVvd7y4PfN6R/yk
cFX8imoCWf+r+R7VXKeCmU3Ai3lOb8bqc7KmP0/by03rlPV6Ztb7foJfbq+Fn5VvnSp/P5b0Mf5j
XDPfunmsBXxoZguy0mYAazdhX/JZO+Uxn9uBQ9L0j4D7zewz/AyqfXr/+vKSuy+9gbfyvMe6wFo5
n8tv8XJd8KK9jYA3JL0s6Xv5MmpmU/GzvH0krQTsm/IPcAse1O5IFZWXSWpfzz7Xp6HPKZ+v7b+k
X0t6PVWSfoz/Ga5e4LbW4pufdTuWfkbgZ4gZn/H172RGIcetULcAv8DL1+/LnVnA/ub7rtf7/ZfU
VtIlkt6SNB8P/qRtdsc/j+z1s6cL+e3V5wOgZ0MLSNpa0lOS5kn6L351k3ts8x4fSRtJejhVfs/H
i6Ey667F1/9PLPu1pB6S7pBUl9a9Nc/75ua1I37VPsrMLs6a9QkebLKtgp+ofZJed8kzL5O3Z83s
SzP7GK9/6gN8q6G8VHVQSc7Fy/Szf0CZSu2VstIK+aI1pHdmIlWCdcMvC2cCz5jZqlmPTmb286x1
rYHtvgt0k9Q5K20d/GxiWXwfeK6eeU8A3SUNwINL5k/6ffzMcN0G8pK7LzPxctpcM/F6h+zPpbOZ
7QVgZlPM7BBgDeBS4J7su/lyDE/53A+YlAINZvaVmZ1nZv3wopvv4WeBBZG0Ff69eT4lfUrj35n/
7b+kHYBTgYOArma2Kn7lrNxl6/Eu3/ysF/H1E55CFHLcCnULcDzwSDrR+J8C9hfy73NDn8OP8OO6
G/6H1ifzdngx8CKgV9byvbOmC/nt1WcE0EtSTQPL3I7XdfY2s1XwOic1sHy2a/E6k75m1gU/ocqs
O5uv/58oZ78uwj+zzdK6hzb0vpJWxG8wmIVfoWabiBfNZZbdAL/yeNPMPkp52Txr+c3TOg1p8DOo
+qCS/mDuxO/gyKTNw39Qh6YzoSPJ/8fXFHtJ2l7SCsAF+BnBTPxKaSNJP5HUPj22ktRgNM/K60y8
COdiSR0kfRs/i7+14TW/Ke3repL+jF/enlfPe36FV47+Hg+OT6T0xcBdwIWSOktaF/hlI3m5Afi1
pC3TLZobpvVGAwsknSapY8rbpumPHEmHSupuZkvwykzwyuR87sDruX7O0gCIpJ0lbZbuqJuP/7HW
t43/kdQlXRndgRfDvJZmjQUOkLSSpA3x49CQzvif3jygnaRz+PpZ3xygj+q/bXk48H/pmHXC/0zu
NLNFje1DtmYet/q2NQ3YCS8eytXY/jZHZ7wu4gM8oF+UlZfFeDn+0HRMNuHrJw0N/vbkt9tPr2c/
p+D1mMPlt1SvkH5/B0vKlHx0xksRvpA0EA+ATdmv+cAnKd/Zge5fQH9JB6S74U7i6ycwnfGriP9K
Whv4TX1vkq7M78FLVg5Pv6dst+FX+Tukk7YLgHuzSkZuBs6S1DV9bsfgRfZI6i9pQPrtdgIux/9X
X29ox6s+qCTn45V22Y7BD8YHQH/8j3tZ3I5fFX2IV3IdCpAOzh7AwSyt0LoUr2Qr1CH4Gdq7eJHD
uWb2ZBPW30bSJ/iX+Gn8h75V1p9lPrfjZ4d35/yJnYifsb+Nn8HfDtxY30bM7G7gwrTcAvyMqVv6
Q/geXnE4DT+bvgE/GwWv85mY8v0nvCz683reYzZesb8tfgKRsSb+g5qPf9Gfwc+06/OQpAX4Ge6Z
+I/kp1nzr8DrJubgt2be1sC2wIveHsMrxWfgFaTZxTN3p+cPJL2SZ/0bU36fxT+jL/DPvzmadNwa
YmbPm9m7eWY1tr/NcXPaVh1+5+ConPm/wL8z7+Gf1XA8CBXy2+uN361Yn5PweoK/4Cc2b+FX+A+l
+ccD56fvzDl44C7Ur/EgtACvzP/f99bM3sdvcLkE/3/qm5PP8/C7G/+LB6B7G3ifzBX6HsDHWtqe
ZIf0XhPxYrvb8DsMV077lXFu2u8Z+H/HZWb2WJrXI+V7Pv69Whe/E/OrhnZcqTImhBAqnqRLgTXN
7PAClv03fhNJg2fWobgiqIQQKlYqOloBv6tpK7y919Fmdn9ZMxbqVUmtW0MIIVdnvMhrLbxY8o94
24tQoeJKJYQQQtG0lor6EEIIFaDVFn+tvvrq1qdPn3JnI4QQqsqYMWPeN7PuzV2/1QaVPn36UFtb
W+5shBBCVZE0o/Gl6hfFXyGEEIomgkoIIYSiiaASQgihaCKohBBCKJoIKiGEEIomgkoIIYSiiaAS
QgihaCKoVJLPPoMbb4TP8/YAH0IIFS+CSiW57jo46ijYdVeYN6/cuQkhhCaLoFJJRo6Ebt3g1Vdh
0CB4441y5yiEEJokgkqlWLQInnkGfvADePpp+OQT2GYbnw4hhCoRQaVSvPIKzJ8Pu+wCW28NL70E
a60Fe+wBw4aVO3chhFCQCCqVYuRIfx482J/79IEXXoAdd4QjjoCzz4YY+yaEUOEiqFSKkSNhs81g
jTWWpq26Kjz6qFfe/+538OMfwxdflC+PIYTQiAgqlWDhQnj+eS/6ytW+PVx/PVx8MQwfDrvtBu+/
3/J5DCGEAkRQqQQvveRtU/IFFQAJTj8d7rwTamv9zrA332zZPIYQQgFKHlQktZX0qqSH0+tukp6Q
NCU9d81a9gxJUyVNlrRnVvqWkl5L866SpFLnu0WNHAlt2nj9SUMOOgieesor9AcNghEjWiZ/IYRQ
oJa4UjkZeD3r9enACDPrC4xIr5HUDzgY6A8MAa6R1Datcy1wDNA3PYa0QL5bzsiRsOWWXofSmG22
gVGjYM01vSjsl7+MFvghhIpR0qAiqRewN3BDVvJ+QOYe2WHA/lnpd5jZQjObBkwFBkrqCXQxs1Fm
ZsDNWetUv08/9SCx666Fr7P++vDyy3DCCXDFFR6QYujkEEIFKPWVypXAqcCSrLQeZjY7Tb8H9EjT
awMzs5abldLWTtO56d8g6VhJtZJq51VLNyfPPw9ffVV/fUp9Vl4Zrr4aHn98aXHYeef5tkIIoUxK
FlQkfQ+Ya2Zj6lsmXXkUrfGFmV1nZjVmVtO9e/dibba0Ro70O7y226556++xB7z2Ghx8MAwdCttu
G927hBDKppRXKtsB+0qaDtwB7CLpVmBOKtIiPc9Ny9cBvbPW75XS6tJ0bnrrMHKk15OstFLzt9G1
K9x6K9x9N0ybBltsAX/6EyxZ0vi6IYRQRCULKmZ2hpn1MrM+eAX8SDM7FHgQODwtdjjwQJp+EDhY
0oqS1sMr5EenorL5kgalu74Oy1qnun30kXfP0tSir/oceCBMmOAV+Kec4s8zZhRn2yGEUIBytFO5
BNhd0hRgt/QaM5sI3AVMAh4DTjCzxWmd4/HK/qnAW8CjLZ3pknj2Wb+aKFZQAb8r7MEH4YYbvDJ/
s82i77AQQouRtdL+pGpqaqy20u+IOvlkby3/8cewwgrF3/60ad5v2LPPwhNP+JVLCCE0QNIYM6tp
7vrRor6cRo6EHXYoTUABWG89+Pe/Yd11vUV+1LGEEEosgkq5zJnj9R/FLPrKZ8UV4fzzYcwYr8gP
IYQSiqBSLpnBt0odVMB7N95sMzjzzGjHEkIoqQgq5TJyJKyyit/+W2pt23ovx2+95XU4IYRQIhFU
ymXkSNhpJ2jXrmXeb6+9vMPK88/3oYpDCKEEIqiUwzvvwNSpLVP0lSHBpZd6Xc4VV7Tc+4YQlisR
VMrhqaf8uSWDCnj/YN//Pvz+91AtfaOFEKpKBJVyGDkSuneH/v1b/r0vush7Rr7wwpZ/7xBCqxdB
paWZeVDZeWcfmKulbbIJHHkkXHONN44MIYQiiqDS0qZOhVmzWr7oK9vQoX5H2DnnlC8PIYRWKYJK
S8sMAVzOoLL22t5FzG23wbhx5ctHCKHViaDS0kaOhF69YMMNy5uP007z4YvPOKO8+QghtCoRVFrS
kiV+59euu/otvuXUtasHlEcfXdq6P4QQllEElZY0YQK8/355i76y/eIXftV02ml+A0EIISyjCCot
aeRIf9555/LmI6NjR29hP3o03HdfuXMTQmgFSjlGfQdJoyWNkzRR0nkpfaikOklj02OvrHXOkDRV
0mRJe2albynptTTvqjQCZPUZORL69oXevRtftqUcdhj06+dFYYsWlTs3IYQqV8orlYXALma2OTAA
GCJpUJp3hZkNSI9HACT1w4cd7g8MAa6R1DYtfy1wDD7EcN80v7osWgTPPFM5RV8Zmc4m33wTbryx
3LkJIVS5Uo5Rb2aW6bmwfXo0VHC/H3CHmS00s2n40MEDJfUEupjZKPNhKm8G9i9VvkvmlVdg/vzK
CyoA++wD223n7Vc++6zcuQkhVLGS1qlIaitpLDAXeMLMXkqzTpQ0XtKNkrqmtLWBmVmrz0ppa6fp
3PR873espFpJtfMqrW+rTH3K4MFlzUZeElxyCcyeHZ1NhhCWSUmDipktNrMBQC/8qmNTvChrfbxI
bDbwxyK+33VmVmNmNd27dy/WZotj5EgfKGuNNcqdk/y23x7+3/+D3/3Oi8JCCKEZWuTuLzP7GHgK
GGJmc1KwWQJcDwxMi9UB2TXYvVJaXZrOTa8eCxfC889XZtFXtj//GTp0gKOPjvHsQwjNUsq7v7pL
WjVNdwR2B95IdSQZ3wcmpOkHgYMlrShpPbxCfrSZzQbmSxqU7vo6DHigVPkuiZdegs8/r/yg0rMn
XH45PPcc/O1v5c5NCKEKlXLYwZ7AsHQHVxvgLjN7WNItkgbglfbTgZ8BmNlESXcBk4BFwAlmtjht
63jgJqAj8Gh6VI+RI71H4h13LHdOGnfEETB8OJx6Kuy9N6yzTrlzFEKoIrJW2pK6pqbGamtry50N
t9NOfqUyenS5c1KY6dNh001hhx3gkUfK36VMCKHFSBpjZjXNXT9a1LeEN96AAQPKnYvC9enjbVce
ewxuvbXcuQkhVJEIKqX25Zcwd653N19NTjjB266ccoqPax9CCAWIoFJqs2f7c69eDS9Xadq0gRtu
8KGHTzyx3LkJIVSJCCqlVpfufq62KxXwoYfPPRfuvjs6nAwhFCSCSqnNSp0BVGNQAfj1r70+6Pjj
4aOPyp2bEEKFi6BSatV8pQLQvr13NDlvHvzqV+XOTQihwkVQKbW6Om+l3rVr48tWqi228IG8/vEP
+Pe/y52bEEIFi6BSanV1fpVS7W09zj7b61iOPRY++aTx5UMIy6UIKqVWV1d9d37l06ED/P3v8M47
8Nvfljs3IYQKFUGl1DJXKq3Bttv67cVXXw0vvFDu3IQQKlAElVIya11BBeDCC2HddeGoo+Djj8ud
mxBChWk0qEjaQNKKaXqwpJMyvQ+HRnzwgXd735qCSqdOfjfY22/7gGPR2j6EkKWQK5V/AoslbQhc
h495cntJc9VaVPvtxPXZeWd46CGYMsUH95o2rdw5CiFUiEKCyhIzW4SPffJnM/sN3q19aExrDSoA
e+4JI0b41dh228GECY2vE0Jo9QoJKl9JOgQ4HHg4pbUvXZZakUxQaQ13f+UzaBA8+6xP77gjvPhi
efMTQii7QoLKT4FtgAvNbFoalfGWxlaS1EHSaEnjJE2UdF5K7ybpCUlT0nPXrHXOkDRV0mRJe2al
bynptTTvqjQCZOWrq/P2KWuuWe6clM6mm/qdYKutBrvtBo8/Xu4chRDKqNGgYmaTgNOAV9LraWZ2
aQHbXgjsYmabAwOAIZIGAacDI8ysLzAivUZSP+BgoD8wBLgmjRoJcC1wDD7EcN80v/LNmgU9enhX
J63ZeuvB889D376wzz5w553lzlEIoUwKuftrH2As8Fh6PUDSg42tZy7T9Lp9ehiwHzAspQ8D9k/T
+wF3mNlCM5sGTAUGpjHtu5jZKPNhKm/OWqeytbbbiRvSowc8/bQXiR1yCPz1r+XOUQihDAop/hoK
DAQ+BjCzscD6hWxcUltJY4G5wBNm9hLQw8zSICO8B/RI02sDM7NWn5XS1k7TuemVb3kKKgCrrurF
X3vvDT//ubdpaaXDVYcQ8iuoot7M/puTtqSQjZvZYjMbAPTCrzo2zZlv+NVLUUg6VlKtpNp58+YV
a7PN11q6aGmKjh3h3nvh0EPhrLO8Z+MlBX1dQgitQLsClpko6UdAW0l9gZOA/zTlTczsY0lP4XUh
cyT1NLPZqWhrblqsDm8Dk9ErpdWl6dz0fO9zHd6WhpqamvKeIn/+OXz44fJ1pZLRvj0MG+aV91dc
AQsWwHXXVX+nmiGERhVypXIiXnm+EG/0+F/glMZWktQ90/JeUkdgd+AN4EH89mTS8wNp+kHgYEkr
pjvM+gKjU1HZfEmD0l1fh2WtU7nefdefl8egAj4c8RVXwJln+rDEv/xlFIWFsBxo9ErFzD4DzkyP
pugJDEt3cLUB7jKzhyW9CNwl6ShgBnBQep+Jku4CJgGLgBPMbHHa1vHATUBH4NH0qGzVPuJjMUhw
wQXeVf6VV8Iqq8DQoeXOVQihhBoNKpKeAH5gZh+n113xu7T2bGg9MxsPbJEn/QNg13rWuRC4ME96
LbDpN9eoYK25NX1TSHD55V4Edt550LlzjCAZQitWSJ3K6pmAAmBmH0lao4R5ah0iqCzVpo3XqSxY
4GPed+7sg32FEFqdQoLKEknrmNk7AJLWpYh3bLVadXX+59mlS7lzUhnatoVbb4VPP4XjjvPP5pBD
yp2rEEKRFRJUzgSel/QMIGAHIE4zG7O8tVEpxAorwD33wHe/Cz/5Cay8Muy7b7lzFUIoogbv/kp3
W00EvgPcCdwBbGlm0cFTYyKo5Nexo3ebv+WWcNBB3tNxCKHVaDCopMaJj5jZ+2b2cHq830J5q26z
ZkVQqU/nzvDoo95X2H77Re/GIbQihbRTeUXSViXPSWuyZAnMnh1BpSHdusETT0DPnrDXXjB2bLlz
FEIogkLqVLYGfixpBvApXq9iZvbtkuasms2dC4sWRVBpzJprwpNPwg47wB57wHPPwcYbe2X+7Nn1
P+bO9f7Fzj/fbwAIIVSMQoJKg+1RQh6tfXCuYlp33aWBZcst/fbjBQu+uVz79h6Eevb0O+ouushH
m7ztNujUqeXzHULIq5AW9TMkbY7f9QXwnJmNK222qly0UWmajTbyCvvLL/f6lp49v/no1s0DTsaf
/wynnOIjTj70UHzWIVSIQlrUn4wPkHVvSrpV0nVm9ueS5qyaRVBpuk03hRtvLHz5E0+E9deHgw+G
rbeGhx+GAQNKl78QQkEKqag/CtjazM4xs3OAQXiQCfWZNcvL+teIjgdKau+9fcRJCbbfHv71r3Ln
KITlXiFBRcDirNeLU1qoT12dF9lEJXLpbb45vPSSV/Dvuy9cdVW5cxTCcq2Qivp/AC9Jui+93h/4
e+my1ApEw8eWtdZa8Oyz8OMfw8knw5Qp3u1+u0K+3iGEYmr0SsXMLgd+CnyYHj81sytLnbGqtjyO
+FhuK68M//yn94B89dV+1TJ/frlzFcJyp9GgIukqoIOZXZUer7ZAvqpbXKmUR9u28Ic/wLXXwr//
7fUs77xT7lyFsFwppE5lDHCWpLck/UFSTakzVdUWLPAz5Agq5XPccfDIIzBjht8Z9swz5c5RCMuN
Qoq/hpnZXsBWwGTgUklTGltPUm9JT0maJGliujUZSUMl1Ukamx57Za1zhqSpkiZL2jMrfUtJr6V5
V6WOLitT3E5cGfbYA/7zH2/3sssu3vp+8eLG1wshLJNCrlQyNgQ2AdbFx5pvzCLgV2bWD78N+QRJ
/dK8K8xsQHo8ApDmHQz0B4YA16ShiAGuxW9j7pseQ5qQ75YVQaVy9O8PY8b4uC3nnuuBZvbscucq
hFatkDqVy9KVyfnABKDGzPZpbD0zm21mr6TpBcDrQEP/tPvhwxQvNLNpwFRgoKSeQBczG5V6Tb4Z
vwOtMkVQqSydO8Mtt3jDyhdf9AaSTzxR7lyF0GoVcqXyFrCNmQ0xs39kDy1cKEl98PHqX0pJJ0oa
L+nGNOY9eMCZmbXarJS2dprOTc/3PsdKqpVUO2/evKZmszgiqFQeCX76U3j5ZVh9ddhzTzjzTO/0
M4RQVPUGFUmbpMmXgXUkfSf7UegbSOoE/BM4xczm40VZ6wMDgNnAH5ud+xxmdp2Z1ZhZTffu3Yu1
2aapq4OuXWGllcrz/qF+/ft7YDnySO+QcuedYebMxtcLIRSsodZhv8LrMfL96RuwS2Mbl9QeDyi3
mdm9AGY2J2v+9cDD6WUd0Dtr9V4prS5N56ZXphicq7KttBLccIMHlOOO8+KwYcPge98rd85CaBXq
vVIxs2PS8855HoUEFOEt719PDSgz6T2zFvs+Xk8D8CBwsKQVJa2HV8iPNrPZwHxJg9I2DwMeaOJ+
tpxoo1Idfvxjr8Tv3Rv22ccbTX75ZblzFULVq/dKRdIBDa2YufJowHbAT4DXJGWG9fstcIikAfjV
znTgZ2l7EyXdBUzC7xw7wcwy94AeD9wEdAQeTY/KVFcH347xy6rCRhvBqFEeUC6/3Md1ue46b9sS
QmiWhoq/Mnd4rQFsC4xMr3cG/sPSrvDzMrPnyd/x5CMNrHMhcGGe9Fpg04beryIsWgRz5sSVSjXp
0AH+8he/3fiEE2CbbeD44+HCC2GVVZZt259/7kNLr7xycfIaQhWoN6iY2U8BJP0b6JeKoTLFVze1
SO6qzXvQMVGAAAAgAElEQVTv+Z9I9PtVffbbz+tZzjrL+w677z7v8fiAA/zusaaYPNnXHTbMh0bu
1MlHrezRw59zp9dcE/r0gXLdXBJCERXSjWvvTEBJ5gDrlCg/1S1uJ65uXbp4MDj0UPjZz+DAA72+
5eqrYZ1GvvJmXnx25ZXeRcwKK3ijy299y0823nvPr2InTYKRI+Gjj76+ftu2fqV03nmw6qql28cQ
SqyQoDJC0uPA8PT6h8CTpctSFZuVmtNEUKluAwf6rcd/+hOccw706+fdvJx00je70//sM7j1Vl92
0iQfmG3oUL+zrEeP+t9j4UIPMnPmeMD51798iOThw+Hii71dTZumdHgRQmUopO+vXwB/BTZPj+vM
7MRSZ6wqxZVK69GunVfgT5oEgwf79MCBUFvr82fNgjPO8LvHfvYzWHFFL+565x3vEqahgAK+/Drr
wFZb+dXQX//qd6NttBEcfTQMGuSDj4VQZQo6FTKz+8zs/9LjvsbXWE7V1Xmxx+qrlzsnoVjWXRce
egjuvtuvKLbe2ute+vSByy7zgPPMMx4QDjvMg0VzbbEFPPecdysza5YHliOP9KuZEKpEXF8XU12d
j0JYwZ0oh2aQvH7l9de9WOvtt+GUU+Ctt3xgsB13LN4xl7xOZ/JkOPVUL1rbaCOvq/nqq+K8Rwgl
JO+jsfWpqamx2kxRRUvZeWe/rfi551r2fUPrNXmyB7DHHvO6nauugl13LXeuQismaYyZNXvcrIb6
/hqRni9t7saXO9GaPhTbxhv73WQPPABffAG77eZ1NiFUqIaKv3pK2hbYV9IWze1QcrlhFv1+hdKQ
YN99YeJELxq74IIYzTJUrIZuKT4HOBvvwPHynHkFdSi5XPn4Y29BHUEllEqHDnDttd61zGGHwfjx
y97qP4Qia6hDyXvM7LvAZc3pUHK5E7cTh5bQqZNX3tfVwS9+Ue7chPANhbRTuUDSvpL+kB7RR3g+
EVRCS9l6azj7bA8ud91V7tyE8DWFDCd8MXAy3nvwJOBkSReVOmNVJxNUot+v0BLOPNODy3HHLe3J
IYQKUEg7lb2B3c3sRjO7ERgCxNVKrkxQWWut8uYjLB/atfNGkgsXwhFHeEemIVSAQhs/ZvdwFzWD
+cya5b3MrrBCuXMSlhd9+8IVV8CIEd5+JYQKUEhQuRh4VdJNkoYBY8gz5kkuSb0lPSVpkqSJkk5O
6d0kPSFpSnrumrXOGZKmSposac+s9C0lvZbmXZVGgKws0UYllMMxx/hQyKefDhMmNL58CCVWSEX9
cGAQPijXP4FtzOzOAra9CPiVmfVL658gqR9wOjDCzPoCI9Jr0ryDgf54Eds1ktqmbV0LHIMPMdw3
za8sEVRCOUhwww3ebf+hh3pxWAhlVGiHkrPN7MH0eK8J67ySphcArwNrA/sBw9Jiw4D90/R+wB1m
ttDMpgFTgYFpULAuZjbKvE+Zm7PWqRx1dVFJH8qjRw/4+99h3Djvqj+EMmqRDiUl9QG2AF4CemQN
+vUekOkjfG1gZtZqs1La2mk6Nz3f+xwrqVZS7bx584qW/0YtXAjz5sWVSiifffbxorDf/z5a24ey
KnlQkdQJLzY7xczmZ89LVx5F69HSzK4zsxozq+nekkOzzk4xMoJKKKfLL4cNNvDW9v/9b7lzE5ZT
DQYVSW0lvdHcjUtqjweU28zs3pQ8JxVpZca7n5vS64DeWav3Sml1aTo3vXLEiI+hEnTq5LcZ19XB
iTGOXiiPBoOKmS0GJktq8pj06Q6tvwOvm1l232EPAoen6cOBB7LSD5a0oqT18Ar50amobL6kQWmb
h2WtUxmiNX2oFIMGecPIW26J1vahLAoZo74rMFHSaODTTKKZ7dvIetsBPwFekzQ2pf0WuAS4S9JR
wAzgoLS9iZLuwlvtLwJOSEEN4HjgJqAj8Gh6VI4IKqGSnHUWPPqoj3M/bJi3vN96ax+6uFu3cucu
tHKFBJWzm7NhM3seqK89Sd5RhszsQvK0gTGzWmDT5uSjRdTVwUorwaqrNr5sCKXWvj3ccw+cd573
aPzooz40A3iDya23hoED/XnzzZdtCOQQcjQaVMzsGUnrAn3N7ElJKwFtG1tvuZJpo1KBbTLDcmqd
dfw2Y4D586G2Fl56yR9PPumdUYL3ALHFFvCjH3k/YtEjRFhGhXQoeQxwD/C3lLQ2cH8pM1V1YnCu
UMm6dIFddoEzzoD774d334V33oG774aTTvJ+w04+2YcrvueepVc1ITRDIbcUn4DXj8wHMLMpwBql
zFTVidb0oZpI0Ls3HHigt2t56SUfsrhDB/jBD2C77eA//yl3LkOVKiSoLDSzLzMvJLWjiG1Lqp6Z
n/lFUAnVSoLvfhfGjoXrr4fp0z2wHHggTJ1a7tyFKlNIUHlG0m+BjpJ2B+4GHipttqrI++/Dl19G
UAnVr107OPpomDLFK/kfe8yLxE4+2b/nIRSgkKByOjAPeA34GfAIcFYpM1VVYnCu0NqsvLL3ITZl
it+WfPXVsOGGcNll8MUX5c5dqHCF3P21JHV5/xJe7DU5da8SINqohNarZ0/429+8Mv+00/xxySU+
EN0qq/gt9NnPuWmDBkHXro2/T2hVGg0qkvYG/gq8hbc7WU/Sz8ysshoglkt00RJau/794eGHYeRI
GD4cPvzQ+xabMwfefBM+/thff/XV19dbZRU49VQvPlt55fLkPbS4Qho//hHY2cymAkjaAPgXldaq
vVzq6qBNG1hzzXLnJITS2mUXf+Rj5kVjmQAzezZceaV3GXPVVXD22d6LcrSDafUKqVNZkAkoydvA
ghLlp/rU1fl4Fu0Kic8htFISdOzoRWabbAI77wwPPAAvvAAbbwy/+IWn33orLF7c+PZC1ao3qEg6
QNIBQK2kRyQdIelw/M6vl1ssh5Uu2qiEUL9tt4Wnn/auYlZdFX7yExgwAB56KBpZtlINXanskx4d
gDnATsBg/E6wjiXPWbWIER9DaJgEQ4Z4VzF33OGD2u27r7eFiQHFWp16y2zM7KctmZGqVVcHO+1U
7lyEUPnatIEf/hAOOAD+8Q9vCzN4sBeV7babd3K51VZewR+qViF3f60HnAj0yV6+gK7vW7/PPoOP
PorirxCaon17OPZYLwq7+mrv+PLMM32e5HUvmV6UBw6Eb3/b1wlVoZDa5fvxwbYeApaUNjtVJtqo
hNB8HTvCb37jj48+gpdfhtGjl/ZFNmyYL9ehA3znOx5gfvxjqKkpb75DgwoJKl+Y2VUlz0k1iqAS
QnF07Qp77OEP8Er8GTOWdtc/ejT89a9+m/JBB8FFF8EGG5Q3zyGvQm4p/pOkcyVtI+k7mUdjK0m6
UdJcSROy0oZKqpM0Nj32ypp3hqSpkiZL2jMrfUtJr6V5V6UhhStDBJUQSkOCPn28Dubyy+H5572x
5dlne0PMTTaBE0+EuXPLndOQo5CgshlwDD4M8B/T4w8FrHcTMCRP+hVmNiA9HgGQ1A84GOif1rlG
UmYgsGvT+/dNj3zbLI8IKiG0nC5d4Pzzvefko46Ca6/1q5ULLoBPP218/dAiCgkqPwDWN7OdzGzn
9KinWe1SZvYs8GGB+dgPuMPMFprZNGAqMFBST6CLmY1K/Y3dDOxf4DZLr67Ov+idO5c7JyEsP3r2
9KKwCRNg992988sNN/R+yhYtKnfulnuFBJUJQDEHXz9R0vhUPJbpbW5tYGbWMrNS2tppOjc9L0nH
SqqVVDtv3rwiZrkeMeJjCOWzySZw773ean+DDXw45M0289Eto2Fl2RRSUb8q8Iakl4GFmcRm3lJ8
LXAB3tvxBXhR2pHN2E5eZnYdcB1ATU1N6b9V0Zo+hPLbdlt47jl48EE4/XT4/vdh0019dMvOnRt/
9OvnXS2FoigkqJxbrDczszmZaUnXAw+nl3VA76xFe6W0ujSdm14Z6upg113LnYsQggT77Qd77+0N
K++8E+bNg7ffhgUL/PHJJ/VfwWyyiTdi3nFHf46TxWYrZDyVovWjIKmnmc1OL7+PF60BPAjcLuly
YC28Qn60mS2WNF/SIHw8l8OAPxcrP8tk8WLviTW+fCFUjnbtvDfkY4755rwlS7zBcibILFjgvSqP
GePdxQwf7vUy4MVpO+209LHuui27H1WskBb1C1g6Jv0KQHvgUzPr0sh6w/G+wlaXNAu/4hksaUDa
3nR8JEnMbKKku4BJwCLgBDPLdGV6PH4nWUe8u/3K6HJ/7lwPLNHvVwjVoU0b6NTJHz17Lk3fdVcf
92XxYhg71gPMM8/AfffBjTf6Muuu61dBl10WY8M0Qk0ZxDG1EdkPGGRmp5csV0VQU1NjtbW1pXuD
2lrvp+iBB7xzvBBC67JkCbz22tIgc//9/pv/179gtdXKnbuSkTTGzJrdbUEhd3/9j7n7gT0bXbi1
m5luVovirxBapzZtYPPNfTjlf/7TH2PHwg47LP39h28opPjrgKyXbYAa4IuS5ahavP66P/ftW958
hBBaxv77w+OPe8nEttvCv/8N3/pWuXNVcQq5Utkn67EnPurjfqXMVFUYPx7WW88bP4YQlg877eRF
YV99Bdtv7/2Sha8p5O6vGFcln/HjvUvuEMLyZcAAb3C5xx6wyy7eAHPPqBHIqDeoSDqngfXMzC4o
QX6qw+efw+TJcOCB5c5JCKEcNtjAA8uQIbDPPt5N/yGHlDtXFaGh4q9P8zwAjgJOK3G+KtukSX5n
yOablzsnIYRyWXNNLwrbZhsf5+XPldGErtwaGk74j5lpSZ2Bk4GfAnfg3assv8aP9+co/gph+bbK
Kl55f8ghfpfYvHk+THIFjdDR0hqsqJfUTdLvgPF4APqOmZ1mZsv3IAbjx8NKK8H665c7JyGEcuvQ
Ae6+27vjv+ACOP54b0i5nGqoTuX3wAF4B42bmdknLZarSjdunHdY17Zt48uGEFq/du3g+uthjTXg
4ou9iPzaa72zyuVMQ1cqv8L74ToLeDf1wTVf0gJJ81smexXILO78CiF8k+TDHP/jH94Sf/PNvdfk
5WwAsXqDipm1MbOOZtbZzLpkPTo31u9XqzZ7NnzwQVTShxDyO+IIvzv00EPh0kuhf3/vln850aRu
WgJRSR9CaFz37n7F8uyz3oHlfvv5Y8aMcues5CKoNFUmqGy2WXnzEUKofDvsAK++6r0bP/mkd+ty
ySXw5ZflzlnJRFBpqnHjfES5rl0bXzaEENq3h9/8xvsL3HNPOOMM2GILb+PSCkVQaarx46M+JYTQ
dOus42O0PPSQDxY2eDD85CcwdWq5c1ZUJQsqkm6UNFfShKy0bpKekDQlPXfNmneGpKmSJkvaMyt9
S0mvpXlXpTFdymPhQnjjjahPCSE03/e+BxMn+hXLPffAxht7cMn0fF7lSnmlchMwJCftdGCEmfUF
RqTXSOoHHAz0T+tcIynTCORa4Bh8iOG+ebbZct54AxYtiqASQlg2K63ktx+//Tb83/95p5T9+8NB
By2tt61SJQsqZvYs8GFO8n7AsDQ9DNg/K/0OM1toZtOAqcBAST2BLmY2ynyIypuz1ml548b5cwSV
EEIx9OwJf/gDTJ/ubVoee8yL1/ffH8aMKXfumqWl61R6mNnsNP0e0CNNrw1kD6U2K6WtnaZz0/OS
dKykWkm18+bNK16uM8aP9y4ZYmCuEEIxde/uVy7Tp8O553olfk0N7LUXvPhiuXPXJGWrqE9XHlbk
bV5nZjVmVtO9e/dibtqNH++XqO0aHYYmhBCarls3GDrU27NcdBG8/LKPMrnrrvD3v/vtyRV+O3JL
B5U5qUiL9JzpmLIO6J21XK+UVpemc9PLI7pnCSG0hC5dvCJ/+nT44x+9Ev/oo+E73/HGlFtu6a+v
uQZGjfK7ySpESweVB4HD0/ThwANZ6QdLWlHSeniF/OhUVDZf0qB019dhWeu0rDlz/BFBJYTQUlZe
GX75S5g1C6ZMgTvv9NerrQb33w8nnODjuXTu7J3cHnYYXHllWfsbK1k5jqThwGBgdUmzgHOBS4C7
JB0FzAAOAjCziZLuAiYBi4ATzCzTd/Tx+J1kHYFH06PlRfcsIYRyadMGNtzQHwcd5GlmMHOmF4m9
8oo/RoyA4cPh5z8vW1ZLFlTMrL6xNXetZ/kLgQvzpNcCmxYxa80TQSWEUEkkb1C5zjrer1jGBx/A
iiuWLVvRor5Q48fDWmvB6quXOychhFC/1VYr69tHUCnUuHFxlRJCCI2IoFKIr77ykdwiqIQQQoMi
qBRi8mQPLNGRZAghNCiCSiGikj6EEAoSQaUQ48b5mAgbb1zunIQQQkWLoFKI8eOhXz8PLCGEEOoV
QaUQMTBXCCEUJIJKY95/H959N+pTQgihABFUGvPaa/4cQSWEEBoVQaUxMTBXCCEULIJKY8aPhzXW
gB49Gl82hBCWcxFUGhOV9CGEULAIKg1ZtAgmToyirxBCKFAElYZMmQJffBFBJYQQClSWoCJpuqTX
JI2VVJvSukl6QtKU9Nw1a/kzJE2VNFnSni2W0eieJYQQmqScVyo7m9kAM6tJr08HRphZX2BEeo2k
fsDBQH9gCHCNpLYtksPx46FdO/jWt1rk7UIIodpVUvHXfsCwND0M2D8r/Q4zW2hm04CpwMAWydH4
8bDJJmUdRS2EEKpJuYKKAU9KGiPp2JTWw8xmp+n3gMw9vGsDM7PWnZXSvkHSsZJqJdXOmzdv2XMZ
A3OFEEKTlGyM+kZsb2Z1ktYAnpD0RvZMMzNJ1tSNmtl1wHUANTU1TV7/az76CGbOjKASQghNUJYr
FTOrS89zgfvw4qw5knoCpOe5afE6oHfW6r1SWmllumeJNiohhFCwFg8qklaW1DkzDewBTAAeBA5P
ix0OPJCmHwQOlrSipPWAvsDokmc07vwKIYQmK0fxVw/gPkmZ97/dzB6T9DJwl6SjgBnAQQBmNlHS
XcAkYBFwgpktLnkux42D1VaDnj1L/lYhhNBatHhQMbO3gW+UKZnZB8Cu9axzIXBhibP2dePH+1WK
B78QQggFqKRbiivH4sUwYUIUfYUQQhNFUMnn7bfhs8+ikj6EEJoogko+MYZKCCE0SwSVfMaPhzZt
oF+/cuckhBCqSgSVfMaPh402go4dy52TEEKoKhFU8omBuUIIoVkiqOSaPx+mTYv6lBBCaIYIKrky
3bNEUAkhhCaLoJIrumcJIYRmi6CSa/x4WHVV6N278WVDCCF8TQSVXNE9SwghNFu5xlOpXFtvDb16
lTsXIYRQlSKo5Lr88nLnIIQQqlYUf4UQQiiaCCohhBCKJoJKCCGEoqmaoCJpiKTJkqZKOr3c+Qkh
hPBNVRFUJLUF/gJ8F+gHHCIpuhAOIYQKUxVBBRgITDWzt83sS+AOYL8y5ymEEEKOagkqawMzs17P
SmlfI+lYSbWSaufNm9dimQshhOCqJagUxMyuM7MaM6vp3r17ubMTQgjLnWpp/FgHZHfG1Sul1WvM
mDHvS5rRzPdbHXi/metWota2P9D69qm17Q+0vn1qbfsD+fdp3WXZoMxsWdZvEZLaAW8Cu+LB5GXg
R2Y2sUTvV2tmNaXYdjm0tv2B1rdPrW1/oPXtU2vbHyjNPlXFlYqZLZL0C+BxoC1wY6kCSgghhOar
iqACYGaPAI+UOx8hhBDq16oq6ovounJnoMha2/5A69un1rY/0Pr2qbXtD5Rgn6qiTiWEEEJ1iCuV
EEIIRRNBJYQQQtFEUMnSGjutlDRd0muSxkqqLXd+mkPSjZLmSpqQldZN0hOSpqTnruXMY1PUsz9D
JdWl4zRW0l7lzGNTSOot6SlJkyRNlHRySq/mY1TfPlXlcZLUQdJoSePS/pyX0ot+jKJOJUmdVr4J
7I53A/MycIiZTSprxpaRpOlAjZlVbaMtSTsCnwA3m9mmKe0y4EMzuySdAHQ1s9PKmc9C1bM/Q4FP
zOwP5cxbc0jqCfQ0s1ckdQbGAPsDR1C9x6i+fTqIKjxOkgSsbGafSGoPPA+cDBxAkY9RXKksFZ1W
Vigzexb4MCd5P2BYmh6G/+CrQj37U7XMbLaZvZKmFwCv433zVfMxqm+fqpK5T9LL9ulhlOAYRVBZ
qqBOK6uQAU9KGiPp2HJnpoh6mNnsNP0e0KOcmSmSEyWNT8VjVVNUlE1SH2AL4CVayTHK2Seo0uMk
qa2kscBc4AkzK8kxiqDS+m1vZgPwsWhOSEUvrYp5GW61l+NeC6wPDABmA38sb3aaTlIn4J/AKWY2
P3tetR6jPPtUtcfJzBan/4JewEBJm+bML8oxiqCyVJM7rawGZlaXnucC9+HFfK3BnFTunSn/nlvm
/CwTM5uTfvRLgOupsuOUyun/CdxmZvem5Ko+Rvn2qdqPE4CZfQw8BQyhBMcogspSLwN9Ja0naQXg
YODBMudpmUhaOVUyImllYA9gQsNrVY0HgcPT9OHAA2XMyzLL/LCT71NFxylVAv8deN3MLs+aVbXH
qL59qtbjJKm7pFXTdEf8hqQ3KMExiru/sqTbA69kaaeVF5Y5S8tE0vr41Ql4P2+3V+M+SRoODMa7
6Z4DnAvcD9wFrAPMAA4ys6qo/K5nfwbjRSoGTAd+llXWXdEkbQ88B7wGLEnJv8XrIKr1GNW3T4dQ
hcdJ0rfxivi2+MXEXWZ2vqTVKPIxiqASQgihaKL4K4QQQtFEUAkhhFA0EVRCCCEUTQSVEEIIRRNB
JYQQQtFEUAlfI2lx6n11YurR9FeSivY9kXSEpLWyXt8gqV+xtp/n/VaU9GTapx/mzLtJ0meZtjwp
7UpJJmn1ZXzf8yXttizbaGT7fbJ7OS5wnU3S5/CqpA2KnJ+bJE1L35k3Jd0sqVfW/Ecy7SRC6xZB
JeT63MwGmFl/vIHUd/F2FAVLPT7X5wjgf0HFzI4ucU/QW6T3GWBmd+aZP5XUcWgKnrvQxJ4UcvdX
UlszO8fMnmxelktmf+AeM9vCzN5qbGG5pvxH/MbMNgc2Bl4FRqaGxJjZXqkld7NJarcs64eWEUEl
1Ct17XIs8Iv0B3OEpKsz8yU9LGlwmv5E0h8ljQO2kXSOpJclTZB0XVr/QKAGuC2dMXeU9LSkmrSN
Q+Rjv0yQdGnW+3wi6cJ0FjxK0jc6vZOPC3F/6uhvlKRvS1oDuBXYKr1fvrPzO4DMFcxg4AVgUdZ2
75d3xjlRWR1y5tnf6ZIulfQK8IN05n5gWvYbn0VK3yrld6yk32euPOQd//0+rTNe0s/qOUTtJN0m
6XVJ90haKa2/paRnUr4fl9RT3rD3FODnkp5Ky/0y5WmCpFNSWh/5mEI3463Fe0vaQ9KLkl6RdLe8
P6x6pR5xr8A7KPxu2u50SatLukTSCVmf41BJv07fj9+nvLymdFUpabCk5yQ9CExKaYelz2WcpFtS
WndJ/0yf2cuStmsoj6GEzCwe8fjfAx8rIjftY7z30iOAq7PSHwYGp2nDW+Nm5nXLmr4F2CdNP42P
70L2a/zq5R2gO976fySwf9a2M+tfBpyVJ49/Bs5N07sAY9P0YODhevb1JuBAYBTQFe/LaSe8pfTq
2fsBdMT/ZFerZ3+nA6fmbruRz2ICsE2avgSYkKaPzewjsCJQC6yXk/c+KQ/bpdc3Ar/GuzT/D9A9
pf8Q7x0CYCjw6zS9Jd5afGWgEzARv6rrg7cgH5SWWx14Fh+LA+A04Jz6PsuctCuB07I+n9XTezyT
tcwkvM+9/wc8gbf47pG+Cz3T8fs0s/9Af3zco9zjczveeSp46/DXy/1bWl4fcTkZimUx3vlexs6S
TgVWArrhf1oPNbD+VsDTZjYPQNJtwI54dyxf4gEMfLCk3fOsvz3+x4SZjZS0mqQuBeb9Xryvt62B
3KuCkyR9P033BvoCH/DN/QXIV7wGeT4LSc8Bnc3sxbTM7cD30vQewLczVzrAKul9p+Vsd6aZvZCm
bwVOAh4DNgWeSBdEbfHedHNtD9xnZp8CSLoX2AHvC2qGmY1Kyw0C+gEvpO2tALz4zc3lpdwEM3tV
0hryerXuwEdmNlPSL4HhZrYY7+TwGfw7MR8YbWaZfd8FuNvSoHO2tEuR3YB+KY8AXSR1sqVjiIQW
EkElNEjef9hivPfSRXy9yLRD1vQX6Q8BSR2Aa/ArkpnyUQ2zl22qryydgqa8FPt7eycerIaZ2ZLM
H5O8aG83/GriM0lPs3Q//re/WT7N3XAzPwsBJ5rZ440sl9vHkqV1J5rZNo2s25Ds/RA+9sYhzdjO
FsCIPOl341eIa1J/IK4vP/Vpg19dfVF49kIpRJ1KqJek7sBf8SKvTAd6AyS1kdSb+rv9zvxpvp/K
3w/MmrcA6PzNVRgN7JTK3dviHfc904TsPgf8OOV7MPC+5YzpUR8zmwGcif/5Z1sFP5P+TNIm+Fl7
U+X9LMwrrRdI2jrNPzhrncfxuo/2aX82kvcynWsdSZng8SN8iNjJQPdMuqT2kvrnWfc5YH9JK6Vt
fz+l5RoFbCdpw7S9lSVt1NAOp/qRk/Diq8fyLHJn2t8D8QCTyc8PU31Sd/wqdXSedUfidVarpffq
ltL/DZyYlYcBDeUxlE5cqYRcHeWjw7XHr0xuATJdf7+AF8FMwodXfSXfBszsY0nX43UG7+HDCmTc
BPxV0ufANlnrzJaPkf0Ufnb8LzNrSjfcQ4EbJY0HPmNpd94FMbO/5Ul+DDhO0uv4n/WoPMs0tt2G
PoujgOslLcED6H9T+g143cYr8sumeeQf5nUyPvDajfgxudbMvkzFZldJWgX/jV+JFz9m5+sVSTex
9I/7hlQ01SdnuXmSjgCGS1oxJZ+F12vk+r2ks/FivlHAzuZDc+d+JhPlt3HX2dIefu/Dvw/j8Cuu
U83svRTMc9e9EHhG0mL8LrMj8KK/v6Tj3w6vBzouTx5DiUUvxSGUSXaZfwqoPc3s5DJnK4RlElcq
IZTP3pLOwH+HM/Az7hCqWlyphBBCKJqoqA8hhFA0EVRCCCEUTQSVEEIIRRNBJYQQQtFEUAkhhFA0
/8TubY8AAAAFSURBVB9zPEXY/8GrugAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The graph shows a sharp incline in the first few years after marriage, then a gradual decline in divorces with higher marriage durations.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">canadaDivorces</span> <span class="o">=</span> <span class="n">divorcesByDurationOfMarriage</span>
<span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorcesByDurationOfMarriage</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>
<span class="n">canadaDivorces</span> <span class="o">=</span> <span class="n">canadaDivorces</span><span class="p">[(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="mi">2005</span><span class="p">)]</span>

<span class="c1"># Removing unnecessary categories</span>
<span class="n">canadaDivorces</span> <span class="o">=</span> <span class="n">canadaDivorces</span><span class="p">[(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;1 to 4&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;5 to 9&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;10 to 14&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;15 to 19&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>  
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;20 to 24&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;25 to 29&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                              <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;all years&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)</span> <span class="o">&amp;</span>
                               <span class="p">(</span><span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;not&#39;</span><span class="p">)</span> <span class="o">==</span> <span class="o">-</span><span class="mi">1</span><span class="p">)]</span>

<span class="n">xs</span> <span class="o">=</span> <span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;Duration of marriage&#39;</span><span class="p">]</span>
<span class="n">xs</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="nb">map</span><span class="p">(</span><span class="nb">int</span><span class="p">,</span> <span class="n">xs</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39; &#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">))</span>
<span class="n">ys</span> <span class="o">=</span> <span class="n">canadaDivorces</span><span class="p">[</span><span class="s1">&#39;VALUE&#39;</span><span class="p">]</span>

<span class="c1">#pl.plot(xs, ys);</span>
<span class="c1">#canadaDivorces[&#39;Duration of marriage&#39;].str.partition(&#39; &#39;)[2].str.partition(&#39; &#39;)[0]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Divorces,-by-reason-for-marital-breakdown">Divorces, by reason for marital breakdown<a class="anchor-link" href="#Divorces,-by-reason-for-marital-breakdown">&#182;</a></h2><p>To gain more insight, let's look at a dataset which covers the reason for divorce.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[115]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">divorcesByReason</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;divorcesByReason.csv&#39;</span><span class="p">)</span>
<span class="c1"># print the size of the dataset</span>
<span class="nb">print</span><span class="p">(</span><span class="n">divorcesByReason</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>

<span class="c1">#Trimming &#39;, reason for marital breakdown&#39; substring from &#39;Reason for marital breakdown&#39; column</span>
<span class="n">divorcesByReason</span><span class="p">[</span><span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorcesByReason</span><span class="p">[</span><span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">2</span><span class="p">]</span>
<span class="n">divorcesByReason</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">divorcesByReason</span><span class="p">[</span><span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39; reason for marital breakdown&#39;</span><span class="p">,</span>
                                                                          <span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="s1">&#39;total&#39;</span> 

<span class="c1">#Trimming &#39;, place of occurence&#39; substring from &#39;GEO&#39; column</span>
<span class="n">divorcesByReason</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">divorcesByReason</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">partition</span><span class="p">(</span><span class="s1">&#39;,&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>(140, 15)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">divByR</span> <span class="o">=</span> <span class="n">divorcesByReason</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="s1">&#39;VALUE&#39;</span><span class="p">,</span> <span class="n">ascending</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="n">xs</span> <span class="o">=</span> <span class="n">divByR</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="mi">2005</span><span class="p">)</span> 
                <span class="o">&amp;</span> <span class="p">(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span> <span class="o">!=</span> <span class="s1">&#39;total&#39;</span><span class="p">)]</span><span class="o">.</span><span class="n">index</span>
<span class="n">ys</span> <span class="o">=</span> <span class="n">divByR</span><span class="o">.</span><span class="n">loc</span><span class="p">[(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="mi">2005</span><span class="p">)</span> 
                <span class="o">&amp;</span> <span class="p">(</span><span class="n">divByR</span><span class="p">[</span><span class="s1">&#39;Reason for marital breakdown&#39;</span><span class="p">]</span> <span class="o">!=</span> <span class="s1">&#39;total&#39;</span><span class="p">),</span> <span class="s1">&#39;VALUE&#39;</span><span class="p">]</span>
<span class="n">colors</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;green&#39;</span><span class="p">,</span> <span class="s1">&#39;orange&#39;</span><span class="p">]</span>
<span class="n">reasons</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;separation for at</span><span class="se">\n</span><span class="s1">least one year&#39;</span><span class="p">,</span> <span class="s1">&#39;adultery&#39;</span><span class="p">,</span> <span class="s1">&#39;physical</span><span class="se">\n</span><span class="s1">cruelty&#39;</span><span class="p">,</span> <span class="s1">&#39;mental</span><span class="se">\n</span><span class="s1">cruelty&#39;</span><span class="p">]</span>

<span class="n">reasonPlot</span> <span class="o">=</span> <span class="n">pl</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">xs</span><span class="p">,</span> <span class="n">ys</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="n">colors</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">xs</span><span class="p">,</span> <span class="n">reasons</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Number of Divorces&quot;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Number of Divorces vs Reason for Marital Breakdown,</span><span class="se">\n</span><span class="s1">Canada 2005&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
z5HvP6+kT84rurYEtgauzUNlSyXtmld9HVKXp1bW/sAVzc6nmJlZZ3X0RH12uf0Wej7/+gTK87Sn
UJ4ncQBARMyTNAO4mdKb61ERsSLzHEnpRXUM5QT9JZl+BjA9T+o/RM9O88zMbJCNuA4lu7q6wld/
mZn1j6Q5EdHV13S+o97MzNrGQcXMzNpmsG5+fF7QCH+g6gg7UmpmA+CWipmZtY2DipmZtY2DipmZ
tY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2D
ipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtY2DipmZtU1Hg4qk9SSdL+lWSbdI2k3S
BpIuk3R7vq9fmf5YSfMl3SZp70r6TpLm5riTpfK0eElrSjo306+RNKmTy2NmZs11uqXyHeDXEfFS
YHvgFuAYYFZEbA3Mys9I2haYDGwH7AOcImlUlnMqcDiwdb72yfQpwMMRsRXwLeDEDi+PmZk10bGg
Imkc8AbgDICI+FdEPALsC0zLyaYB++XwvsA5EfFkRNwJzAd2kbQxMDYiro6IAM6sy1Mr63xgz1or
xszMBl8nWypbAouBH0u6QdLpktYGJkTEvTnNfcCEHJ4ILKzkvzvTJuZwfXqPPBGxHHgU2LC+IpKO
kNQtqXvx4sVtWTgzM3u2TgaV0cCOwKkR8SrgcfJQV022PKKDdajN57SI6IqIrvHjx3d6dmZmI1Yn
g8rdwN0RcU1+Pp8SZO7PQ1rk+wM5fhGwWSX/ppm2KIfr03vkkTQaGAcsafuSmJlZSzoWVCLiPmCh
pJdk0p7AzcBM4NBMOxT4eQ7PBCbnFV1bUk7IX5uHypZK2jXPlxxSl6dW1v7AFdn6MTOzITC6w+V/
DDhL0hrAHcAHKIFshqQpwF3AAQARMU/SDErgWQ4cFRErspwjganAGOCSfEG5CGC6pPnAQ5Srx8zM
bIhopO3Yd3V1RXd394DyjvTrykbYpmJmFZLmRERXX9P5jnozM2sbBxUzM2sbBxUzM2sbBxUzM2sb
BxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUz
M2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2sbBxUzM2ubjgYVSQskzZX0Z0nd
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
1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYOKmZm1jYO
KmZm1jYOKmZm1jYOKmZm1jYdCyqSfiTpAUk3VdI2kHSZpNvzff3KuGMlzZd0m6S9K+k7SZqb406W
pExfU9K5mX6NpEmdWhYzM2tNJ1sqU4F96tKOAWZFxNbArPyMpG2BycB2mecUSaMyz6nA4cDW+aqV
OQV4OCK2Ar4FnNixJTEzs5Z0LKhExO+Ah+qS9wWm5fA0YL9K+jkR8WRE3AnMB3aRtDEwNiKujogA
zqzLUyvrfGDPWivGzMyGxmCfU5kQEffm8H3AhByeCCysTHd3pk3M4fr0HnkiYjnwKLBhZ6ptZmat
GLIT9dnyiMGYl6QjJHVL6l68ePFgzNLMbEQa7KByfx7SIt8fyPRFwGaV6TbNtEU5XJ/eI4+k0cA4
YEmjmUbEaRHRFRFd48ePb9OimJlZvcEOKjOBQ3P4UODnlfTJeUXXlpQT8tfmobKlknbN8yWH1OWp
lbU/cEW2fszMbIiM7lTBks4G9gA2knQ38AXgBGCGpCnAXcABABExT9IM4GZgOXBURKzIoo6kXEk2
BrgkXwBnANMlzadcEDC5U8tiZmat0Ujbue/q6oru7u4B5R3p15aNsE3FzCokzYmIrr6m8x31ZmbW
Ng4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4q
ZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNg4qZmbWNh17Rr3Zs/h5zENd
A7OOc0vFzMzaxkHFzMzaxkHFzMzaZtgHFUn7SLpN0nxJxwx1fczMRrJhfaJe0ijge8BbgLuB6yTN
jIibh7ZmZh3w0xF+oQPAf6zaxQ46fmSvw/hC5y8WGe4tlV2A+RFxR0T8CzgH2HeI62RmNmIN65YK
MBFYWPl8N/Dq+okkHQEckR+XSbptEOrWCRsBDw7VzJ8HVwQP6fp7PqxAhnodHjTs1+HQ/oaPW6X1
t0UrEw33oNKSiDgNOG2o67GqJHVHRNdQ12O48vpbdV6Hq2YkrL/hfvhrEbBZ5fOmmWZmZkNguAeV
64CtJW0paQ1gMjBziOtkZjZiDevDXxGxXNL/Ay4FRgE/ioh5Q1ytThr2h/CGmNffqvM6XDXP+/Wn
cH9EZmbWJsP98JeZmT2HOKiYmVnbOKg8x0haT9KRlc+bSDq/TWW/XtI8SX+WNKYdZVbK/oSkF7Sz
zBbne5ik7/YxzSRJN+XwDpLeNji1GxkkfbbF6RZI2qjT9RkM7VgWSV2STh5g3tmSnpOXJjuoDAFJ
zS6QWA94JqhExD0RsX+bZn0Q8LWI2CEinuhr4j7qWe8TwKAHlQHYAehXUOnnehiJWgoq1lNEdEfE
0UNdj3ZzUEmS1pb0S0k3SrpJ0oGZvpOkKyXNkXSppI0zfbak7+Re/02Sdsn0XST9SdINkv4o6SWZ
fpikmZKuAGZJWkfSLEnXS5orqda9zAnAi7Pck+r2steS9OOc/gZJb6yU/TNJv5Z0u6SvN1i+DwEH
AF+SdJaKk7LucyvLu4ek30uaCTyrDzVJp0rqzhbP8Zl2NLAJ8FtJv23ftwKSLsp1Py97RkDSByT9
VdK1wGsr006VtH/l87K6stYAvggcmOv3wPzefyTp2lyn++a09d/XmZL2q5R1VuU7GxZyW7o119Nf
cxneLOmq3G526WN9PGsbk3QCMCbX51mZ9qzvbLiqrLOzJN0i6XytbJF/rPL7famk1XLdjM+8q6l0
dDte0nvzt3ajpN/l+D0kXZzD61R+23+R9J5Mf9bv7TkvIvwqV8C9B/hh5fM4YHXgj8D4TDuQctky
wOza9MAbgJtyeCwwOoffDFyQw4dRupHZID+PBsbm8EbAfEDApFpZOW5Spez/qsz/pcDfgbWy7Duy
zmsBdwGbNVjGqcD+leW9jHIp9oQsa2NgD+BxYMte1lOt/qNyHbwyPy8ANurA91Kb3xjgJkrXPH8H
xgNrAFcB361fvvy8rME6PKw2fX7+KnBwDq8H/BVYu8H3tTtwUWXbuLP2PQ+XV66H5cArKDuUc4Af
5Xa3L3BRH+uj4TZWW89NvrMNO7mNDMI6C+C1+flHwKdyWT6WaUcCp+fwF4BP5PBerPz9zwUm1tZr
vu8BXJzDJwLfrsx3/bp1Wf97mw10DfX6afRyS2WlucBbJJ0o6fUR8SjwEuDlwGWS/gx8jnLXfs3Z
ABHxO2CspPUoP7rzsnXxLWC7yvSXRcRDOSzgq5L+AlxO+bOc0EcdXwf8JOd5K+WHvU2OmxURj0bE
PyktjL766XkdcHZErIiI+4ErgZ1z3LURcWcv+Q6QdD1wQy7btn3MZ1UdLelG4GpK7wnvB2ZHxOIo
nYieu4rl7wUck9/vbMof5uY57pnvKyKupNxoOx54H+XPYvkqznso3BkRcyPiaWAeZbsJyvY/iebr
o9VtrP4727pTCzNIFkbEVTn8E8pvB+Bn+T6Hsu6gBJ1DcviDwI9z+CpgqqTDKQGi3pspPa4DEBEP
5+Bg/95WmY8Vp4j4q6QdKcfbvyxpFnAhMC8idustW4PPXwJ+GxHvkjSJ8sOsebwyfBBlb3uniHhK
0gLKD3ignqwMr2DVvtvHGyVK2pKyl7ZzRDwsaSqrVuemJO1B+bHtFhH/kDQbuJXef1jLyUO6klaj
tGT6nA3wnojo0cmopFfz7PVwJnAwpeeGD7S2FM851e3k6crnpynbzAp6Xx99bmO9fGcd20YGSaPf
OaxcH8+si4hYKOl+SW+i9KJ+UKZ/JNfhvwNzJO3U10wH+/fWLm6pJEmbAP+IiJ8AJwE7ArcB4yXt
ltOsLqna8qidh3gd8Gi2bsaxsv+xw5rMchzwQAaUN7Jyr+8xYN1e8vye3EglbUPZgxxoj8u/p5xb
GJV7328Aru0jz1jKH+2jkiYAb62Ma1bvgRoHPJx/Ti8FdqUcUtld0oaSVgfeW5l+AVD7sb6Tcviy
Xn09L6UcGxeApFc1qc9UygUJxPP3mT39WR81T+V3AY2/s+Fu89p/APAfwB/6mP50SovmvIhYASDp
xRFxTUR8HlhMzz4LoRyKPqr2QdL6NP+9PWc5qKz0CuDabPZ/AfhyHl7ZHzgxm/N/Bl5TyfNPSTcA
3wemZNrXga9lerPWwllAl6S5lObyrQARsQS4Kk/qnVSX5xRgtcxzLnBYRDzJwFwI/AW4EbgC+HRE
3NcsQ0TcSGmG3wr8lNKkrzkN+LXae6L+18BoSbdQLmC4GrgXOA74U87/lsr0P6QEnBuB3Wjc4vot
sG2eWD6Q0rJcHfiLpHn5uaE8THgLKw9pPB+1vD4qTsvpz6Lxdzbc3QYclcu0PnBqH9PPBNah53Zy
Up6Ev4lynvbGujxfBtavncwH3tjH7+05y920DFA26z8VEd1DXRcbHHnVz1xgx2yV2vNcHsK+OCJe
3o88XcC3IuL1narXc5lbKmYtkPRmSivl/xxQrDeSjgEuAI4d6roMFbdUzMysbdxSaYHqbqJrQ3mH
5YUBZsOesssS1XUxZK15vq0/B5WhcRjlDvRhTVKj6+1tmNKqd0fTo4uhkcbrr3BQ6SdJ/y3puuxK
4fhKeqPuREapdIlR6wrlP1W6EekCzlKDjh1VOjy8Osu/MC8trHULc6JK9xl/lfT6yjxOqtTpww3q
/EVJn6h8/oqkj/d3eTJ9maRvVK6wsmFE0iH5Xd8oaXpun9+XdA3wdUnHSfpUZfqb8mQ1kg7O7e/P
kn7QYKeivouhYd+1TT2vvxYM9S39w+HFyu4+9qJcPilKQL4YeEP07E7hma4pKPdMXFYpp9Y9w2x6
6WKBcpnv7jn8RbLrhszzjRx+G3B5Dh8BfC6H1wS6qetihXK37/U5vBrwt6xfv5YnPwdwwFB/J34N
aDvejtLtyka175hy783FwKhMO45yVWMtz025/bwM+AWweqafAhySwwsoXQ1NomcXQ8O+axuvv/6/
fEd9/+yVrxvy8zqULih+R+ma4l2ZXuua4jbgRZL+D/gl8JtmhUsaRwk8V2bSNOC8yiSNuoXYC3il
VnakOC7n/Uw3KxGxQNISlRvZJgA3RMQSSf1dniWUu4cvaLYc9pz1JsoNeQ8CRMRDKvc4PnOTXhN7
UnaSrss8Y4AHmmWIiCslnaJyc+17GL5d29R4/bXAQaV/ROk6/gc9EnvpmiJK1wrbA3sDH6H0EvzB
VZj/s7qFyDp9LCIu7SPv6ZRzOf9G6Z+o38uTo//Zwg/IhpfqTaLPdHWTat+7gGkR0d9LZZ8PXdv0
xeuvwudU+udS4IOS1gGQNFHSC+mlawqVh/isFhEXUDqj3DHLadilSZT7Hx6unS+hdJ54Zf10Der0
UWU3GZK2kbR2g+kuBPahdBp5aSVvy8tjw94VwHslbQggaYMG0ywgt1OVvvC2zPRZwP65fSBpA0n1
HUo22q6n8vzp2sbrrwVuqfRDRPxG0suAP2UTdhllL+LXwEdUunG4jZVdU0wEfqzSuSGsvCFqKvB9
SU9QWgPVB2YdmuNeQOlqvK+9k9PJcyYqlVoM7Fc/UUT8S6ULlUdqLY0BLI8NYxExT9JXgCslrWDl
Yc+qC4BDVLpouYZyDoGIuFnS54Df5Pb8FKWvqrsq5S9ReTbLTcAlEfHfEXF/bkcXdXbpOs/rrzW+
+XGEyA35euC9EXH7UNfHRga5a5tVMhzXnw9/jQCStqU8BGyWA4oNFrlrm1UyXNefWypmZtY2bqmY
mVnbOKiYmVnbOKiYmVnbOKiYmVnbOKiYmVnbOKiYmVnb/P+f26e3xyAeeAAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We can see that seperation for at least one year is by far the most common reason given for marital breakdown, with <strong>67526</strong> cases. Adultery was second with <strong>2218</strong>. Mental Cruelty was third with <strong>878</strong> cases, and Physical cruelty was fourth with <strong>619</strong> cases.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Number-of-Divorces-By-Year">Number of Divorces By Year<a class="anchor-link" href="#Number-of-Divorces-By-Year">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[116]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">vitalStatsDivorce</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;vitalStatsDivorce.csv&#39;</span><span class="p">)</span>
<span class="c1"># print the size of the dataset</span>
<span class="nb">print</span><span class="p">(</span><span class="n">vitalStatsDivorce</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>(446, 15)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Graph each province/territory&#39;s Divorce Rates by Number of Divorces per year</span>
<span class="n">GEOs</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Ontario&#39;</span><span class="p">,</span> <span class="s1">&#39;Newfoundland and Labrador&#39;</span><span class="p">,</span> <span class="s1">&#39;Prince Edward Island&#39;</span><span class="p">,</span> <span class="s1">&#39;Nova Scotia&#39;</span><span class="p">,</span> <span class="s1">&#39;New Brunswick&#39;</span><span class="p">,</span> <span class="s1">&#39;Quebec&#39;</span><span class="p">,</span>
        <span class="s1">&#39;Manitoba&#39;</span><span class="p">,</span> <span class="s1">&#39;Saskatchewan&#39;</span><span class="p">,</span> <span class="s1">&#39;Alberta&#39;</span><span class="p">,</span> <span class="s1">&#39;British Columbia&#39;</span><span class="p">,</span> <span class="s1">&#39;Yukon&#39;</span><span class="p">,</span> <span class="s1">&#39;Northwest Territories and Nunavut&#39;</span><span class="p">]</span>
<span class="n">colors</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;yellow&#39;</span><span class="p">,</span> <span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="s1">&#39;purple&#39;</span><span class="p">,</span> <span class="s1">&#39;green&#39;</span><span class="p">,</span> <span class="s1">&#39;pink&#39;</span><span class="p">,</span> <span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="s1">&#39;black&#39;</span><span class="p">,</span> <span class="s1">&#39;cyan&#39;</span><span class="p">,</span> <span class="s1">&#39;magenta&#39;</span><span class="p">,</span> <span class="s1">&#39;gray&#39;</span><span class="p">,</span> 
           <span class="s1">&#39;maroon&#39;</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">GEOs</span><span class="p">)):</span>
    <span class="n">pl</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">vitalStatsDivorce</span><span class="p">[(</span><span class="n">vitalStatsDivorce</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">GEOs</span><span class="p">[</span><span class="n">i</span><span class="p">])][</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">],</span>
            <span class="n">vitalStatsDivorce</span><span class="p">[(</span><span class="n">vitalStatsDivorce</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="n">GEOs</span><span class="p">[</span><span class="n">i</span><span class="p">])][</span><span class="s1">&#39;VALUE&#39;</span><span class="p">],</span> 
            <span class="n">color</span><span class="o">=</span><span class="n">colors</span><span class="p">[</span><span class="n">i</span><span class="p">]);</span>
    
<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;Number of Divorces by Year, Canada 1970-2004&quot;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">GEOs</span><span class="p">,</span> <span class="n">loc</span><span class="o">=</span><span class="s1">&#39;center left&#39;</span><span class="p">,</span> <span class="n">bbox_to_anchor</span><span class="o">=</span><span class="p">(</span><span class="mf">1.0</span><span class="p">,</span> <span class="mf">0.5</span><span class="p">))</span>
<span class="n">pl</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;Year&quot;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;Rate per 1,000 Marriages&quot;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
6dLlOgB07NixMCUlxTwnJ8coIyPDLCoq6ioAWFpaCmtr67KffvrJZt++fTZqtVrt6+urPn36dJPE
xES9Jm/tLc7XX389Mysryzg/P99Yo8yNHj06WzO2W7du+fv377f++eefrfr06ZNbWFhonJ+fb3Th
wgVzf3//orKyMnrppZecVSqVunv37qrMzEyzCxcumOhe2759+5qGhITkt2nTpqRJkybiscceu1LV
PQsKCioYPny46wcffGBfUnJ7qcorV64YP/zww+6enp6+r7zyisvJkyfLrzcsLCzPzs6u1NLSUnh4
eNw4ffq0eW1kYKqmOha0DUoUZ3MiGgtgNIDl1VlcCFEKIICImgPYTER+Ov2CiAxu7RJCLAOwDJC1
OA19PoapFqmpQFGR4QME9KFSAWvWAI8+KguuL1t2Z+tduCC3T7t1A8aPl21ubsCBA1LpGj1aBii8
9Zb+hLybN8ut16Ag4KefblXONBgZATNnAmFh0voXGgp89BEwYYK02jENSnUtXXWNxgdNt93S0rKs
ojlmZmbl3wPGxsbi+vXrFRorhBB46aWX0qZPn16nNUe7du1a+Oyzz1ru27evKDIyMi8rK8vk448/
ttdYnpYuXWqbnZ1tcuzYsQRzc3Ph5OTUQSNnZddWHdatW3fu119/bbpt27ZmgYGB6tjY2Fvu34wZ
M5wiIiLy9+zZczopKcmsR48e5duguveuuLiY//gMRHWCBN6H3D7cBMALwBwhxKc1OYkS/fkbpO9Y
BhG1BgDlMVMZdhGAdtSLs9J2UXmu237LHCIyAdAMQDYY5m6gLmpw3gkDBwKvvgosXy63PWuLEFIp
Ky4GvvjiVgWseXNZBH7MGGn9GjZM+pNp8/33/ylnu3bpV860CQuTdUe7d5eF4TnKk6kDWrRoUdaq
VaubX331VXMAuH79OuXn5xv169cv76uvvrLPzc01AoCzZ8+aXrx4sTrGDdjb25daW1uX7tq1ywoA
vvzyS1tNX5MmTUTr1q2Lt2/f3qJHjx4F4eHh+YsXL24VFhaWDwC5ubnG9vb2xebm5mL79u3Wly5d
0pt/tGvXrtcOHTpknZ6eblxUVESbN29uoW+cNsePHzfv0aPHtY8//vhSixYtSs6cOXPL2nl5ecbO
zs43AWDp0qX2Va1XGxmYqqlWPjMhxB4hxHQhxDQhxJ7qzCEiB8VyBiKyANAbQCKAbQCeVoY9DWCr
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
iMmTtY3LUEcKC+HPf5bpzOBgWLQIxo0z/mWNxYEMSZUR3YRRrjabWLMCmth32dUFQoOklZdDUSno
CtDI9KizVWjAWmbnSvmq/CJJxFtXUZV1SgIX/H0h3rI8+niJUNuyB7btPX+qEoPBYGgj1HQF864q
zgAsX7BavXGtSMvXgB1a6xcqvfUBcJO1fhOwrFL/9VZkZnegJ/CdNR2ap5S6yDrmxCr7OI81Flhj
/M8aiY8/hoQEqZt5662SfPW661qXONMadh0UH67cgraVGiI3X6xA4aHgWY+pxraA3S7+bX4+YrUL
8JXUIYH+ZwMLOgZCbCT0jJAgiR92nA1YqInsXNi+XyyBidFgr3QJ6+AnQi+3oPHSjxgMBkMLUdMj
68dKqY+ABZyN4gxHBFKNEZwW/wPcCGxRSm2y+h4AngbeVUrdChwCxgForbcppd4FtgMO4HeV/N3u
QSx6nkhwwMdW/2vAQiugIBu4vg7jMtTE0aMSifmvf0nZoq++kqLkrZG8QskFBuLL5e4GIR2kNbez
en3QWkSluytEhLX0aFoOpWR61NsLtu+DjTsl8W7oeUqB5eSLdczbA5J6ig9bVToGytTx/nRwOyyJ
fQ0Gg6ENcl4LmtZ6CpJm4zLgj1a7DJijtZ5U24G11l9rrZXWOklr3cdqK7TWJ7XWV2ite2qth2qt
syvt84TWOkprHau1/rhS/3qtdaL13iSnlUxrXaK1vlZrHa217q+13l/dWAx1oKJCSjP16gVLl8Jj
j0kus9YqzkDSK9gUXJQklhMfTxFqG3fCt1vEgTy/sPVZUo5mQUEx9Ahv+iLvbQF/H0iJF6vbzgMi
Xiuq5HTLK4CteyQAoHdMzf6PXUOlVFbGcQlcMLRrlFIpo0aN6u58XVZWRocOHZIvu+yy6IYe89JL
L43OysqyZ2Vl2Z9++umQ2rZfvny574Wcz2CojtqiOCtbqwztlS1b4O674T//gcsug7lzW3/KDK0l
j1dggFjOnP5PDodEFZ44JTfo9GPgYTmzdw1teauao1x8z/y8xdJnENxcxW9sf7r83wqKID5K+p0R
mq7WNm6uNR9LKYgKlxxu+9Pl+9ExsHk+h6HZ8fT0rNi1a5dnQUGB8vHx0f/+97/9QkNDyy7kmF98
8cVegF27drm99tprHWfOnFnHqBeDofE4rwVNKeWilLpTKfWxUmqz1T5WSt1lOf8b2jp5eTB1qtST
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
+cs9DzzwQO3q1aunPPfcczsB2trajFdfffUtn8/Hbbfd1hKJROxvfetbHQD/8A//UNfR0eFfv379
W6+//npw5cqVp/z5n/9537nnnpv64x//GL3mmmsG2tvbjc7OTgnwwgsvRK+66qreV199Nfj000/X
rF+//q1AICA/+9nPTn3ooYdqW1tbc21tbf7t27dvAeju7tbr6ursH/3oRw333XffvvPOOy97tDG5
4YYbpj366KN7Fi5cWHj22WfDq1evnvriiy9uB+jo6PC//vrrW3Vd59Zbb23ZsWNH1csvv/xWKBSS
zzzzTBRg4cKFhauvvrqrrq7OuuuuuzoBzjvvvNmf+9znulevXt1733331d1yyy1T1qxZs2v4Pkti
CuCmm26a+rWvfa39ggsuyJQyfdu3b99y3333Nf3oRz/ac/7552cGBga0UCjkDD+Hn/3sZ7sbGxvt
VCqlLV26dP61117bF4/H7XQ6rX/oQx9K/fCHPzxwww03TH7wwQfr7rnnnvabb755ys0339x50003
9d59990Nh4vP1772tc7W1tYFd911V/vh1qtky5YtoTfeeGPL5MmTi0uXLp3/+9//PnzBBRdkvv71
r3d873vfO+g4DitWrJjx9NNPx6688spkJpPRt2/fbsyePdt84oknEitXruwdbd8jxftoURm040Tg
CrGpwBLcF4ZfClzjled57VO99ZQ4UxzCwFvwwqfhN0uh83lo/TZcugvm3zYozkokWuGsx+DS3TD/
L6H9OXj2TPjdObD7n6FnHWQPgHPMPTwKxYSnpqbGWbVqVc+999475Ob92muvhW+88cZegNWrV/du
2LChPKz3sssu6/P5Rs9RXHrppf26rrNs2bJ8T0+PH+CjH/1o+qWXXops2LAhOGfOnFxdXV1xz549
/g0bNoTPP//89Jo1a6KbN28Otba2zp83b96CF154IbZr167AvHnzCvv27Qtcf/31U55++ulYIpE4
ru637u5ufePGjZHLL7981rx58xbceuut0zo7O8svBLz88sv79IppoD7xiU/0hUKhI04ttXHjxvAX
v/jFXoCbb765Z926deX32QzfZ4kXX3wxdsstt0ybN2/eghUrVpwyMDCgp9NpceaZZ6a/+tWvTvn2
t7/d0NfXp48U43vuuadx7ty5C5YvXz6vo6PD2Lp1awDcLsorr7wyCbBs2bLs22+/bQC89tprkRtu
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
TkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>An interesting trend in this data is a significant spike in divorces between 1985 and 1990.</p>
<p>Upon further research, the cause for this spike may have been found:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="The-1986-Divorce-Act">The 1986 Divorce Act<a class="anchor-link" href="#The-1986-Divorce-Act">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In 1986, Canadian Parliament passed the new Divorce Act, replacing the previous version from 1968. From <a href="https://en.wikipedia.org/wiki/Divorce_Act_(Canada)#1986_Act">Wikipedia</a>:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="https://i.imgur.com/vhZb7Zy.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The act made many changes to how divorces were handled by the government. One change was that divorces would be granted on terms that the couple had been seperated for 1 year. Previously this limit had been 3 years.</p>
<p>To further test how the act influenced divorce rates, let's make a plot for Canada as a whole with labelled significant years and come up with a percentage divorce increase between 1985 and 1987:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[98]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1985</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1986</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;orange&#39;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1987</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;green&#39;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">legend</span><span class="p">([</span><span class="mi">1985</span><span class="p">,</span> <span class="mi">1986</span><span class="p">,</span> <span class="mi">1987</span><span class="p">])</span>

<span class="n">pl</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">vitalStatsDivorce</span><span class="p">[(</span><span class="n">vitalStatsDivorce</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)][</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">],</span>
        <span class="n">vitalStatsDivorce</span><span class="p">[(</span><span class="n">vitalStatsDivorce</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)][</span><span class="s1">&#39;VALUE&#39;</span><span class="p">],</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;red&#39;</span><span class="p">);</span>

<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Number of Divorces by Year, Canada&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Number of Divorces&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Year&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
pILyq4j4bW5+XdKIiDiUL20dzu0HOXtU1Z3bSvxN6Q+PVHrQfYeIpEHAd4FfFF4bBEyjMC+Rh7VH
Jd2Qh9d3Ab9vatD0Pe58ueCyfNwBfB5o+uirTtyvAZ/Mrw0jTVruaoN89xh31fMtaWiOF0k3Aicj
YkfV810r7lbkO+fncWBnRDxSeGklMDMfz+RM/lYCt0m6KF+6uxpYX5Wc90ur7xRo9Ub65H4I6CIN
oWcB95E+6bwEzCGvPJD7TwHW9fA+k0i/sHuBnxXPqWrcwDDSnTJbSderf0y+86QKcQMXA8tzbDuA
b7dDvmvF3Qb5HgvsJk0uryYtdd4O+e4x7hbl+6OkS1tbgc15+yxwKfAnYE+O8ZLCObNzXndTuMOr
2Tkva/MyLWZmVhpf/jIzs9K4qJiZWWlcVMzMrDQuKmZmVhoXFTMzK42LilkDKfmLpJsLbbdKeqqV
cZk1im8pNmswSdeSvrcykbSKxSbgMxGx9y285+BI3yQ3qxSPVMwaLNJaa6uA7wAPAQsjYq+kmZLW
58UOf56/KY6kuZI6lZ7H8VD3+0g6IGmOpE3A1Jb8MGa98NpfZs3xMLCRtAjipDx6mQp8JCJOSppL
WpttMem5G0fy0vlrJK2IiB35fQ5HxMRW/ABm58NFxawJIuK4pKXAfyPihKRPAR8COvNq7EM4swT6
7ZJmkf59jiQ9L6S7qCxtbuRmfeOiYtY8p/MG6Wl+8yLiwWIHSVeT1riaHBFvSFoEvKPQ5XhTIjXr
J8+pmLXGamBaYRXdSyW9BxgOHOPMEy5vqvMeZpXjkYpZC0TEi5IeBlbnCfou4OukB03tAHYB+4Dn
WxelWd/5lmIzMyuNL3+ZmVlpXFTMzKw0LipmZlYaFxUzMyuNi4qZmZXGRcXMzErjomJmZqX5P3eA
X0XKd+68AAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">vsd</span> <span class="o">=</span> <span class="n">vitalStatsDivorce</span><span class="p">[(</span><span class="n">vitalStatsDivorce</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)]</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">)[</span><span class="s1">&#39;VALUE&#39;</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;1985 divorces:&#39;</span><span class="p">,</span> <span class="n">vsd</span><span class="p">[</span><span class="mi">1985</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;1986 divorces:&#39;</span><span class="p">,</span> <span class="n">vsd</span><span class="p">[</span><span class="mi">1986</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;1987 divorces:&#39;</span><span class="p">,</span> <span class="n">vsd</span><span class="p">[</span><span class="mi">1987</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;aproximate percentage divorce increase from 1985 to 1987: &#39;</span>
      <span class="p">,</span><span class="nb">int</span><span class="p">(</span><span class="nb">round</span><span class="p">((</span><span class="n">vsd</span><span class="p">[</span><span class="mi">1987</span><span class="p">]</span> <span class="o">-</span> <span class="n">vsd</span><span class="p">[</span><span class="mi">1985</span><span class="p">])</span><span class="o">/</span><span class="n">vsd</span><span class="p">[</span><span class="mi">1985</span><span class="p">]</span> <span class="o">*</span> <span class="mi">100</span><span class="p">)),</span> <span class="s1">&#39;%&#39;</span><span class="p">,</span> <span class="n">sep</span> <span class="o">=</span><span class="s1">&#39;&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>1985 divorces: 61976
1986 divorces: 78304
1987 divorces: 96200
aproximate percentage divorce increase from 1985 to 1987: 55%
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>So there was a 55% increase in divorces due to the 1986 divorce act, but that trend didn't continue long, with divorces dropping down to ~80,000 in the early 90's and ~75,000 in the late 90's/early 2000's.</p>
<p>Measuring the number of divorces alone isn't the best way to analyze this data. To get a better representation, let's adjust for married population. We can find that data from the 'Estimates of population, by marital status, age group and sex for July 1, Canada, provinces and territories' dataset.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[119]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">estPopByMaritalStat</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">&#39;estimatePopulationByMaritalStatus.csv&#39;</span><span class="p">,</span> <span class="n">low_memory</span><span class="o">=</span><span class="kc">False</span><span class="p">);</span>
<span class="c1"># print the size of the dataset</span>
<span class="nb">print</span><span class="p">(</span><span class="n">estPopByMaritalStat</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="c1">#filter data for only married population for all Canada</span>
<span class="n">marriedPopulationCanada</span> <span class="o">=</span> <span class="n">estPopByMaritalStat</span><span class="p">[(</span><span class="n">popByMaritalStatus</span><span class="p">[</span><span class="s1">&#39;GEO&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Canada&#39;</span><span class="p">)</span> <span class="o">&amp;</span> 
                                               <span class="p">(</span><span class="n">popByMaritalStatus</span><span class="p">[</span><span class="s1">&#39;Sex&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Both sexes&#39;</span><span class="p">)</span> <span class="o">&amp;</span>
                                               <span class="p">(</span><span class="n">popByMaritalStatus</span><span class="p">[</span><span class="s1">&#39;Age group&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;All ages&#39;</span><span class="p">)</span> <span class="o">&amp;</span>
                                               <span class="p">(</span><span class="n">popByMaritalStatus</span><span class="p">[</span><span class="s1">&#39;Marital status&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Married&#39;</span><span class="p">)</span> <span class="o">&amp;</span>
                                               <span class="p">(</span><span class="n">popByMaritalStatus</span><span class="p">[</span><span class="s1">&#39;Type of marital status&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Marital status&#39;</span><span class="p">)]</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>(1070880, 18)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[88]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#trim both datasets to include the same years and make new series to hold divorces as a percentage of married population</span>
<span class="n">canadaDivorces</span> <span class="o">=</span> <span class="n">vsd</span><span class="p">[</span><span class="n">vsd</span><span class="o">.</span><span class="n">index</span> <span class="o">&gt;=</span> <span class="mi">1971</span><span class="p">]</span>
<span class="n">canadaMarriedPop</span> <span class="o">=</span> <span class="n">marriedPopulationCanada</span><span class="p">[</span><span class="n">marriedPopulationCanada</span><span class="p">[</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">]</span> <span class="o">&lt;=</span> <span class="mi">2003</span><span class="p">]</span><span class="o">.</span><span class="n">set_index</span><span class="p">(</span><span class="s1">&#39;REF_DATE&#39;</span><span class="p">)[</span><span class="s1">&#39;VALUE&#39;</span><span class="p">]</span>
<span class="n">canadaDivorcesByMarriedPop</span> <span class="o">=</span> <span class="n">canadaDivorces</span> <span class="o">/</span> <span class="n">canadaMarriedPop</span> <span class="o">*</span> <span class="mi">100</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[104]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># plot divorces/married population and years 1985-1987</span>
<span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1985</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;orange&#39;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1986</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;red&#39;</span><span class="p">);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">axvline</span><span class="p">(</span><span class="mi">1987</span><span class="p">,</span> <span class="n">linestyle</span><span class="o">=</span><span class="s1">&#39;:&#39;</span><span class="p">,</span> <span class="n">color</span> <span class="o">=</span> <span class="s1">&#39;green&#39;</span><span class="p">);</span>

<span class="n">pl</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="p">);</span>
<span class="c1">#plot pooints on the line for 1985, 1986 and 1987</span>
<span class="n">pl</span><span class="o">.</span><span class="n">scatter</span><span class="p">([</span><span class="mi">1985</span><span class="p">,</span><span class="mi">1986</span><span class="p">,</span><span class="mi">1987</span><span class="p">],</span> <span class="n">canadaDivorcesByMarriedPop</span><span class="p">[(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="o">.</span><span class="n">index</span> <span class="o">&gt;=</span> <span class="mi">1985</span><span class="p">)</span> 
                                <span class="o">&amp;</span> <span class="p">(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="o">.</span><span class="n">index</span> <span class="o">&lt;=</span> <span class="mi">1987</span><span class="p">)],</span> <span class="n">color</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;orange&#39;</span><span class="p">,</span> <span class="s1">&#39;red&#39;</span><span class="p">,</span> <span class="s1">&#39;green&#39;</span><span class="p">]);</span>
<span class="n">pl</span><span class="o">.</span><span class="n">legend</span><span class="p">([</span><span class="s1">&#39;1985&#39;</span><span class="p">,</span> <span class="s1">&#39;1986, Divorce Act&#39;</span><span class="p">,</span> <span class="s1">&#39;1987&#39;</span><span class="p">]);</span>

<span class="n">pl</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Divorces/Married Population by Year&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Divorces/Married Population (%)&#39;</span><span class="p">)</span>
<span class="n">pl</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Year&#39;</span><span class="p">);</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[108]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Divorces/Married Population:</span><span class="se">\n</span><span class="s1">1985:&#39;</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="p">[</span><span class="mi">1985</span><span class="p">],</span><span class="mi">2</span><span class="p">)</span>
      <span class="p">,</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">1986:&#39;</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="p">[</span><span class="mi">1986</span><span class="p">],</span> <span class="mi">2</span><span class="p">)</span>
      <span class="p">,</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">1987:&#39;</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">canadaDivorcesByMarriedPop</span><span class="p">[</span><span class="mi">1987</span><span class="p">],</span> <span class="mi">2</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>Divorces/Married Population:
1985: 0.49 
1986: 0.61 
1987: 0.74
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The spike is even clearer in this graph, with a .49% Divorce rate in 1985 and .74% in 1987. We can also see that this rate drops quickly and decreases over time. From this, we can extrapolate that the 1986 Divorce Act temporarily increased divorces, but did not have a permanent effect on the divorce rate.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Conclusion">Conclusion<a class="anchor-link" href="#Conclusion">&#182;</a></h1><p>The main point of interest in this data is an obvious correlation between the revised Divorce Act of Canada and the large increase in divorces in 1986, 1987 and 1988. The 1986 Divorce Act removed restrictions for being granted a divorce. It appears that many married couples were divorced because of this. Perhaps they did not meet the 3-year seperation required as cause for divorce that was required prior to 1986.</p>
<p>This trend did not last, however. Divorce rates plunged and levelled off in the early 1990's before dropping again and levelling off in the late 90's/early 2000's.</p>
<p>A conclusion to be drawn from this is that loosening divorce laws can cause temporary rises in divorces, but could be inconsequential in the long term. This analysis could be useful to governments, as it implies that strict divorce laws do not result in lower divorce rates, and loosening divorce restrictions only has short-term consequences. This analysis could be taken to show that government policy has little effect on personal relationships. Perhaps the loosening of divorce restrictions could make the world a better place.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

