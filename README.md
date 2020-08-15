```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /*! nouislider - 9.2.0 - 2017-01-11 10:35:35 */
      /* Functional styling;
      * These styles are required for noUiSlider to function.
      * You don't need to change these rules to apply your design.
      */
      .noUi-target,
      .noUi-target * {
        -webkit-touch-callout: none;
        -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
        -webkit-user-select: none;
        -ms-touch-action: none;
        touch-action: none;
        -ms-user-select: none;
        -moz-user-select: none;
        user-select: none;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
      }
      .noUi-target {
        position: relative;
        direction: ltr;
      }
      .noUi-base {
        background-color: rgba(65, 65, 65, 0.65);
        width: 100%;
        height: 100%;
        position: relative;
        z-index: 1;
        /* Fix 401 */
      }
      .noUi-connect {
        position: absolute;
        right: 0;
        top: 0;
        left: 0;
        bottom: 0;
        border-radius: 5px;
      }
      .noUi-origin {
        position: absolute;
        height: 0;
        width: 0;
      }
      .noUi-handle {
        position: relative;
        z-index: 1;
      }
      .noUi-state-tap .noUi-connect,
      .noUi-state-tap .noUi-origin {
        -webkit-transition: top 0.3s, right 0.3s, bottom 0.3s, left 0.3s;
        transition: top 0.3s, right 0.3s, bottom 0.3s, left 0.3s;
      }
      .noUi-state-drag * {
        cursor: inherit !important;
      }
      /* Painting and performance;
      * Browsers can paint handles in their own layer.
      */
      .noUi-base,
      .noUi-handle {
        -webkit-transform: translate3d(0, 0, 0);
        transform: translate3d(0, 0, 0);
      }
      /* Slider size and handle placement;
      */
      .noUi-horizontal {
        height: 4px;
        cursor: pointer;
      }
      .noUi-horizontal .noUi-handle {
        width: 24px;
        height: 20px;
        left: -17px;
        top: -8px;
      }
      .noUi-vertical {
        width: 18px;
      }
      .noUi-vertical .noUi-handle {
        width: 28px;
        height: 34px;
        left: -6px;
        top: -17px;
      }
      /* Styling;
      */
      .noUi-target {
        background: #FAFAFA;
        border-radius: 5px;
        box-shadow: inset 0 1px 1px #F0F0F0, 0 3px 6px -5px #BBB;
      }
      .noUi-connect {
        background: #33b5e5;
        box-shadow: inset 0 0 3px rgba(51, 51, 51, 0.45);
        -webkit-transition: background 450ms;
        transition: background 450ms;
      }
      /* Handles and cursors;
      */
      .noUi-draggable {
        cursor: ew-resize;
      }
      .noUi-vertical .noUi-draggable {
        cursor: ns-resize;
      }
      .noUi-handle {
        border-radius: 50%;
        background: #33B5E5;
        cursor: pointer;
      }
      .noUi-active {
        /*box-shadow: inset 0 0 1px #FFF, inset 0 1px 7px #DDD, 0 3px 6px -3px #BBB;*/
      }
      /* Handle stripes;
      */

      /*
      .noUi-handle:before,
      .noUi-handle:after {
      content: "";
      display: block;
      position: absolute;
      height: 14px;
      width: 1px;
      background: #E8E7E6;
      left: 14px;
      top: 6px;
      }
      .noUi-handle:after {
      left: 17px;
      }
      .noUi-vertical .noUi-handle:before,
      .noUi-vertical .noUi-handle:after {
      width: 14px;
      height: 1px;
      left: 6px;
      top: 14px;
      }
      .noUi-vertical .noUi-handle:after {
      top: 17px;
      }
      */

      /* Disabled state;
      */
      [disabled] .noUi-connect {
        background: #B8B8B8;
      }
      [disabled].noUi-target,
      [disabled].noUi-handle,
      [disabled] .noUi-handle {
        cursor: not-allowed;
      }
      /* Base;
      *
      */
      .noUi-pips,
      .noUi-pips * {
        -moz-box-sizing: border-box;
        box-sizing: border-box;
      }
      .noUi-pips {
        position: absolute;
        color: #999;
      }
      /* Values;
      *
      */
      .noUi-value {
        position: absolute;
        text-align: center;
      }
      .noUi-value-sub {
        color: #ccc;
        font-size: 10px;
      }
      /* Markings;
      *
      */
      .noUi-marker {
        position: absolute;
        background: #CCC;
      }
      .noUi-marker-sub {
        background: #AAA;
      }
      .noUi-marker-large {
        background: #AAA;
      }
      /* Horizontal layout;
      *
      */
      .noUi-pips-horizontal {
        padding: 10px 0;
        height: 80px;
        top: 100%;
        left: 0;
        width: 100%;
      }
      .noUi-value-horizontal {
        -webkit-transform: translate3d(-50%, 50%, 0);
        transform: translate3d(-50%, 50%, 0);
      }
      .noUi-marker-horizontal.noUi-marker {
        margin-left: -1px;
        width: 2px;
        height: 5px;
      }
      .noUi-marker-horizontal.noUi-marker-sub {
        height: 10px;
      }
      .noUi-marker-horizontal.noUi-marker-large {
        height: 15px;
      }
      /* Vertical layout;
      *
      */
      .noUi-pips-vertical {
        padding: 0 10px;
        height: 100%;
        top: 0;
        left: 100%;
      }
      .noUi-value-vertical {
        -webkit-transform: translate3d(0, 50%, 0);
        transform: translate3d(0, 50%, 0);
        padding-left: 25px;
      }
      .noUi-marker-vertical.noUi-marker {
        width: 5px;
        height: 2px;
        margin-top: -1px;
      }
      .noUi-marker-vertical.noUi-marker-sub {
        width: 10px;
      }
      .noUi-marker-vertical.noUi-marker-large {
        width: 15px;
      }
      .noUi-tooltip {
        display: block;
        position: absolute;
        border: 1px solid #D9D9D9;
        border-radius: 3px;
        background: #fff;
        color: #000;
        padding: 5px;
        text-align: center;
      }
      .noUi-horizontal .noUi-tooltip {
        -webkit-transform: translate(-50%, 0);
        transform: translate(-50%, 0);
        left: 50%;
        bottom: 120%;
      }
      .noUi-vertical .noUi-tooltip {
        -webkit-transform: translate(0, -50%);
        transform: translate(0, -50%);
        top: 50%;
        right: 120%;
      }
    </style>
    <link href="style.css" rel="stylesheet">

    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css?family=Muli" rel="stylesheet">
  </head>
  <body>
    <i class="fa fa-arrow-right fa-2x" id="settings-button"></i>
    <div id="side-menu">

      <div class="section-header">Visualization Style</div>
      <div class="viz-style generic-menu-item">Windmill</div>
      <div class="viz-style generic-menu-item">Frequency Bars</div>
      <div class="viz-style generic-menu-item">Waveform</div>

      <div class="section-header">Style Settings</div>

      <!--	BEGIN WINDMILL SETTINGS	-->
      <div class="viz-settings-visibility">
        <div class="settings-subsection">Style Presets</div>

        <div class="windmill-presets generic-menu-item">Default</div>

        <div class="hide">
          <div class="settings-subsection">Background Gradient Color 1</div>

          <div class="settings-item-container">
            <div class="slider-label">RED <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">GREEN <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">BLUE <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">OPACITY <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-subsection">Background Gradient Color 2</div>

          <div class="settings-item-container">
            <div class="slider-label">RED <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">GREEN <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">BLUE <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">OPACITY <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>
        </div>

        <div class="settings-subsection">Windmill Blades</div>

        <div class="settings-item-container">
          <div class="slider-label">WIDTH FACTOR <strong class="windmill-slider-value slider-value"></strong></div>
          <div class="windmill-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="toggle-label">TOGGLE RAINBOW BLADES</div>
          <label class="switch">
            <input type="checkbox" class="toggle-windmill">
            <div class="toggle-switch"></div>
          </label>
        </div>

        <div id="hidden-windmill-sliders">
          <div class="settings-item-container">
            <div class="slider-label">RED <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">GREEN <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">BLUE <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>

          <div class="settings-item-container">
            <div class="slider-label">OPACITY <strong class="windmill-slider-value slider-value"></strong></div>
            <div class="windmill-slider slider"></div>
          </div>
        </div>

        <div class="settings-subsection">Other Settings</div>

        <div class="settings-item-container">
          <div class="slider-label">CHAOS <strong class="windmill-slider-value slider-value"></strong></div>
          <div class="windmill-slider slider"></div>
        </div>

      </div>
      <!--	END WINDMILL SETTINGS	-->
      <!--	BEGIN FREQUENCY BARS SETTINGS	-->
      <div id="bars-settings" class="viz-settings-visibility">

        <div class="settings-subsection">Style Presets</div>

        <div class="bars-presets generic-menu-item">Blue Sky</div>

        <div class="bars-presets generic-menu-item">Neon Purple</div>

        <div class="bars-presets generic-menu-item">Twilight</div>

        <div class="bars-presets generic-menu-item">Chill Pink</div>

        <div class="settings-subsection">Background Gradient Color 1</div>

        <div class="settings-item-container">
          <div class="slider-label">RED <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">GREEN <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">BLUE <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">OPACITY <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-subsection">Background Gradient Color 2</div>

        <div class="settings-item-container">
          <div class="slider-label">RED <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">GREEN <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">BLUE <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">OPACITY <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-subsection">Bar Color</div>

        <div class="settings-item-container">
          <div class="slider-label">RED <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">GREEN <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">BLUE <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">OPACITY <strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-subsection">Toggle Responsive Bar Colors<p>Changes the respective RGB color value by summing it with the height of the bar. You may have to lower the respective bar color slider to see the effect.</p></div>

        <div class="settings-item-container">
          <div class="toggle-label">RED</div>
          <label class="switch">
            <input type="checkbox" class="freq-bars-responsive">
            <div class="toggle-switch"></div>
          </label>
          <div class="toggle-label">GREEN</div>
          <label class="switch">
            <input type="checkbox" class="freq-bars-responsive">
            <div class="toggle-switch"></div>
          </label>
          <div class="toggle-label">BLUE</div>
          <label class="switch">
            <input type="checkbox" class="freq-bars-responsive">
            <div class="toggle-switch"></div>
          </label>
        </div>

        <div class="settings-subsection">Other Settings</div>

        <div class="settings-item-container">
          <div class="slider-label">BAR COUNT<strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>

        <div class="settings-item-container">
          <div class="slider-label">BAR HEIGHT<strong class="freq-bars-slider-value slider-value"></strong></div>
          <div class="freq-bars-slider slider"></div>
        </div>
      </div>
      <!--END FREQUENCY BARS SETTINGS-->

      <div class="viz-settings-visibility">
      </div>

      <div class="section-header">About</div>
      <div class="generic-menu-item">Created by Justin Chen</div>
      <div class="generic-menu-item">Source on GitHub</div>
    </div>

    <script>


      !function(a){"function"==typeof define&&define.amd?define([],a):"object"==typeof exports?module.exports=a():window.noUiSlider=a()}(function(){"use strict";function a(a,b){var c=document.createElement("div");return j(c,b),a.appendChild(c),c}function b(a){return a.filter(function(a){return!this[a]&&(this[a]=!0)},{})}function c(a,b){return Math.round(a/b)*b}function d(a,b){var c=a.getBoundingClientRect(),d=a.ownerDocument,e=d.documentElement,f=m();return/webkit.*Chrome.*Mobile/i.test(navigator.userAgent)&&(f.x=0),b?c.top+f.y-e.clientTop:c.left+f.x-e.clientLeft}function e(a){return"number"==typeof a&&!isNaN(a)&&isFinite(a)}function f(a,b,c){c>0&&(j(a,b),setTimeout(function(){k(a,b)},c))}function g(a){return Math.max(Math.min(a,100),0)}function h(a){return Array.isArray(a)?a:[a]}function i(a){a=String(a);var b=a.split(".");return b.length>1?b[1].length:0}function j(a,b){a.classList?a.classList.add(b):a.className+=" "+b}function k(a,b){a.classList?a.classList.remove(b):a.className=a.className.replace(new RegExp("(^|\\b)"+b.split(" ").join("|")+"(\\b|$)","gi")," ")}function l(a,b){return a.classList?a.classList.contains(b):new RegExp("\\b"+b+"\\b").test(a.className)}function m(){var a=void 0!==window.pageXOffset,b="CSS1Compat"===(document.compatMode||""),c=a?window.pageXOffset:b?document.documentElement.scrollLeft:document.body.scrollLeft,d=a?window.pageYOffset:b?document.documentElement.scrollTop:document.body.scrollTop;return{x:c,y:d}}function n(){return window.navigator.pointerEnabled?{start:"pointerdown",move:"pointermove",end:"pointerup"}:window.navigator.msPointerEnabled?{start:"MSPointerDown",move:"MSPointerMove",end:"MSPointerUp"}:{start:"mousedown touchstart",move:"mousemove touchmove",end:"mouseup touchend"}}function o(a,b){return 100/(b-a)}function p(a,b){return 100*b/(a[1]-a[0])}function q(a,b){return p(a,a[0]<0?b+Math.abs(a[0]):b-a[0])}function r(a,b){return b*(a[1]-a[0])/100+a[0]}function s(a,b){for(var c=1;a>=b[c];)c+=1;return c}function t(a,b,c){if(c>=a.slice(-1)[0])return 100;var d,e,f,g,h=s(c,a);return d=a[h-1],e=a[h],f=b[h-1],g=b[h],f+q([d,e],c)/o(f,g)}function u(a,b,c){if(c>=100)return a.slice(-1)[0];var d,e,f,g,h=s(c,b);return d=a[h-1],e=a[h],f=b[h-1],g=b[h],r([d,e],(c-f)*o(f,g))}function v(a,b,d,e){if(100===e)return e;var f,g,h=s(e,a);return d?(f=a[h-1],g=a[h],e-f>(g-f)/2?g:f):b[h-1]?a[h-1]+c(e-a[h-1],b[h-1]):e}function w(a,b,c){var d;if("number"==typeof b&&(b=[b]),"[object Array]"!==Object.prototype.toString.call(b))throw new Error("noUiSlider ("+U+"): 'range' contains invalid value.");if(d="min"===a?0:"max"===a?100:parseFloat(a),!e(d)||!e(b[0]))throw new Error("noUiSlider ("+U+"): 'range' value isn't numeric.");c.xPct.push(d),c.xVal.push(b[0]),d?c.xSteps.push(!isNaN(b[1])&&b[1]):isNaN(b[1])||(c.xSteps[0]=b[1]),c.xHighestCompleteStep.push(0)}function x(a,b,c){if(!b)return!0;c.xSteps[a]=p([c.xVal[a],c.xVal[a+1]],b)/o(c.xPct[a],c.xPct[a+1]);var d=(c.xVal[a+1]-c.xVal[a])/c.xNumSteps[a],e=Math.ceil(Number(d.toFixed(3))-1),f=c.xVal[a]+c.xNumSteps[a]*e;c.xHighestCompleteStep[a]=f}function y(a,b,c,d){this.xPct=[],this.xVal=[],this.xSteps=[d||!1],this.xNumSteps=[!1],this.xHighestCompleteStep=[],this.snap=b,this.direction=c;var e,f=[];for(e in a)a.hasOwnProperty(e)&&f.push([a[e],e]);for(f.length&&"object"==typeof f[0][0]?f.sort(function(a,b){return a[0][0]-b[0][0]}):f.sort(function(a,b){return a[0]-b[0]}),e=0;e<f.length;e++)w(f[e][1],f[e][0],this);for(this.xNumSteps=this.xSteps.slice(0),e=0;e<this.xNumSteps.length;e++)x(e,this.xNumSteps[e],this)}function z(a,b){if(!e(b))throw new Error("noUiSlider ("+U+"): 'step' is not numeric.");a.singleStep=b}function A(a,b){if("object"!=typeof b||Array.isArray(b))throw new Error("noUiSlider ("+U+"): 'range' is not an object.");if(void 0===b.min||void 0===b.max)throw new Error("noUiSlider ("+U+"): Missing 'min' or 'max' in 'range'.");if(b.min===b.max)throw new Error("noUiSlider ("+U+"): 'range' 'min' and 'max' cannot be equal.");a.spectrum=new y(b,a.snap,a.dir,a.singleStep)}function B(a,b){if(b=h(b),!Array.isArray(b)||!b.length)throw new Error("noUiSlider ("+U+"): 'start' option is incorrect.");a.handles=b.length,a.start=b}function C(a,b){if(a.snap=b,"boolean"!=typeof b)throw new Error("noUiSlider ("+U+"): 'snap' option must be a boolean.")}function D(a,b){if(a.animate=b,"boolean"!=typeof b)throw new Error("noUiSlider ("+U+"): 'animate' option must be a boolean.")}function E(a,b){if(a.animationDuration=b,"number"!=typeof b)throw new Error("noUiSlider ("+U+"): 'animationDuration' option must be a number.")}function F(a,b){var c,d=[!1];if("lower"===b?b=[!0,!1]:"upper"===b&&(b=[!1,!0]),b===!0||b===!1){for(c=1;c<a.handles;c++)d.push(b);d.push(!1)}else{if(!Array.isArray(b)||!b.length||b.length!==a.handles+1)throw new Error("noUiSlider ("+U+"): 'connect' option doesn't match handle count.");d=b}a.connect=d}function G(a,b){switch(b){case"horizontal":a.ort=0;break;case"vertical":a.ort=1;break;default:throw new Error("noUiSlider ("+U+"): 'orientation' option is invalid.")}}function H(a,b){if(!e(b))throw new Error("noUiSlider ("+U+"): 'margin' option must be numeric.");if(0!==b&&(a.margin=a.spectrum.getMargin(b),!a.margin))throw new Error("noUiSlider ("+U+"): 'margin' option is only supported on linear sliders.")}function I(a,b){if(!e(b))throw new Error("noUiSlider ("+U+"): 'limit' option must be numeric.");if(a.limit=a.spectrum.getMargin(b),!a.limit||a.handles<2)throw new Error("noUiSlider ("+U+"): 'limit' option is only supported on linear sliders with 2 or more handles.")}function J(a,b){if(!e(b))throw new Error("noUiSlider ("+U+"): 'padding' option must be numeric.");if(0!==b){if(a.padding=a.spectrum.getMargin(b),!a.padding)throw new Error("noUiSlider ("+U+"): 'padding' option is only supported on linear sliders.");if(a.padding<0)throw new Error("noUiSlider ("+U+"): 'padding' option must be a positive number.");if(a.padding>=50)throw new Error("noUiSlider ("+U+"): 'padding' option must be less than half the range.")}}function K(a,b){switch(b){case"ltr":a.dir=0;break;case"rtl":a.dir=1;break;default:throw new Error("noUiSlider ("+U+"): 'direction' option was not recognized.")}}function L(a,b){if("string"!=typeof b)throw new Error("noUiSlider ("+U+"): 'behaviour' must be a string containing options.");var c=b.indexOf("tap")>=0,d=b.indexOf("drag")>=0,e=b.indexOf("fixed")>=0,f=b.indexOf("snap")>=0,g=b.indexOf("hover")>=0;if(e){if(2!==a.handles)throw new Error("noUiSlider ("+U+"): 'fixed' behaviour must be used with 2 handles");H(a,a.start[1]-a.start[0])}a.events={tap:c||f,drag:d,fixed:e,snap:f,hover:g}}function M(a,b){if(b!==!1)if(b===!0){a.tooltips=[];for(var c=0;c<a.handles;c++)a.tooltips.push(!0)}else{if(a.tooltips=h(b),a.tooltips.length!==a.handles)throw new Error("noUiSlider ("+U+"): must pass a formatter for all handles.");a.tooltips.forEach(function(a){if("boolean"!=typeof a&&("object"!=typeof a||"function"!=typeof a.to))throw new Error("noUiSlider ("+U+"): 'tooltips' must be passed a formatter or 'false'.")})}}function N(a,b){if(a.format=b,"function"==typeof b.to&&"function"==typeof b.from)return!0;throw new Error("noUiSlider ("+U+"): 'format' requires 'to' and 'from' methods.")}function O(a,b){if(void 0!==b&&"string"!=typeof b&&b!==!1)throw new Error("noUiSlider ("+U+"): 'cssPrefix' must be a string or `false`.");a.cssPrefix=b}function P(a,b){if(void 0!==b&&"object"!=typeof b)throw new Error("noUiSlider ("+U+"): 'cssClasses' must be an object.");if("string"==typeof a.cssPrefix){a.cssClasses={};for(var c in b)b.hasOwnProperty(c)&&(a.cssClasses[c]=a.cssPrefix+b[c])}else a.cssClasses=b}function Q(a,b){if(b!==!0&&b!==!1)throw new Error("noUiSlider ("+U+"): 'useRequestAnimationFrame' option should be true (default) or false.");a.useRequestAnimationFrame=b}function R(a){var b={margin:0,limit:0,padding:0,animate:!0,animationDuration:300,format:V},c={step:{r:!1,t:z},start:{r:!0,t:B},connect:{r:!0,t:F},direction:{r:!0,t:K},snap:{r:!1,t:C},animate:{r:!1,t:D},animationDuration:{r:!1,t:E},range:{r:!0,t:A},orientation:{r:!1,t:G},margin:{r:!1,t:H},limit:{r:!1,t:I},padding:{r:!1,t:J},behaviour:{r:!0,t:L},format:{r:!1,t:N},tooltips:{r:!1,t:M},cssPrefix:{r:!1,t:O},cssClasses:{r:!1,t:P},useRequestAnimationFrame:{r:!1,t:Q}},d={connect:!1,direction:"ltr",behaviour:"tap",orientation:"horizontal",cssPrefix:"noUi-",cssClasses:{target:"target",base:"base",origin:"origin",handle:"handle",handleLower:"handle-lower",handleUpper:"handle-upper",horizontal:"horizontal",vertical:"vertical",background:"background",connect:"connect",ltr:"ltr",rtl:"rtl",draggable:"draggable",drag:"state-drag",tap:"state-tap",active:"active",tooltip:"tooltip",pips:"pips",pipsHorizontal:"pips-horizontal",pipsVertical:"pips-vertical",marker:"marker",markerHorizontal:"marker-horizontal",markerVertical:"marker-vertical",markerNormal:"marker-normal",markerLarge:"marker-large",markerSub:"marker-sub",value:"value",valueHorizontal:"value-horizontal",valueVertical:"value-vertical",valueNormal:"value-normal",valueLarge:"value-large",valueSub:"value-sub"},useRequestAnimationFrame:!0};Object.keys(c).forEach(function(e){if(void 0===a[e]&&void 0===d[e]){if(c[e].r)throw new Error("noUiSlider ("+U+"): '"+e+"' is required.");return!0}c[e].t(b,void 0===a[e]?d[e]:a[e])}),b.pips=a.pips;var e=[["left","top"],["right","bottom"]];return b.style=e[b.dir][b.ort],b.styleOposite=e[b.dir?0:1][b.ort],b}function S(c,e,i){function o(b,c){var d=a(b,e.cssClasses.origin),f=a(d,e.cssClasses.handle);return f.setAttribute("data-handle",c),0===c?j(f,e.cssClasses.handleLower):c===e.handles-1&&j(f,e.cssClasses.handleUpper),d}function p(b,c){return!!c&&a(b,e.cssClasses.connect)}function q(a,b){ca=[],da=[],da.push(p(b,a[0]));for(var c=0;c<e.handles;c++)ca.push(o(b,c)),ia[c]=c,da.push(p(b,a[c+1]))}function r(b){j(b,e.cssClasses.target),0===e.dir?j(b,e.cssClasses.ltr):j(b,e.cssClasses.rtl),0===e.ort?j(b,e.cssClasses.horizontal):j(b,e.cssClasses.vertical),ba=a(b,e.cssClasses.base)}function s(b,c){return!!e.tooltips[c]&&a(b.firstChild,e.cssClasses.tooltip)}function t(){var a=ca.map(s);$("update",function(b,c,d){if(a[c]){var f=b[c];e.tooltips[c]!==!0&&(f=e.tooltips[c].to(d[c])),a[c].innerHTML=f}})}function u(a,b,c){if("range"===a||"steps"===a)return ka.xVal;if("count"===a){if(!b)throw new Error("noUiSlider ("+U+"): 'values' required for mode 'count'.");var d,e=100/(b-1),f=0;for(b=[];(d=f++*e)<=100;)b.push(d);a="positions"}return"positions"===a?b.map(function(a){return ka.fromStepping(c?ka.getStep(a):a)}):"values"===a?c?b.map(function(a){return ka.fromStepping(ka.getStep(ka.toStepping(a)))}):b:void 0}function v(a,c,d){function e(a,b){return(a+b).toFixed(7)/1}var f={},g=ka.xVal[0],h=ka.xVal[ka.xVal.length-1],i=!1,j=!1,k=0;return d=b(d.slice().sort(function(a,b){return a-b})),d[0]!==g&&(d.unshift(g),i=!0),d[d.length-1]!==h&&(d.push(h),j=!0),d.forEach(function(b,g){var h,l,m,n,o,p,q,r,s,t,u=b,v=d[g+1];if("steps"===c&&(h=ka.xNumSteps[g]),h||(h=v-u),u!==!1&&void 0!==v)for(h=Math.max(h,1e-7),l=u;l<=v;l=e(l,h)){for(n=ka.toStepping(l),o=n-k,r=o/a,s=Math.round(r),t=o/s,m=1;m<=s;m+=1)p=k+m*t,f[p.toFixed(5)]=["x",0];q=d.indexOf(l)>-1?1:"steps"===c?2:0,!g&&i&&(q=0),l===v&&j||(f[n.toFixed(5)]=[l,q]),k=n}}),f}function w(a,b,c){function d(a,b){var c=b===e.cssClasses.value,d=c?m:n,f=c?k:l;return b+" "+d[e.ort]+" "+f[a]}function f(a,b,c){return'class="'+d(c[1],b)+'" style="'+e.style+": "+a+'%"'}function g(a,d){d[1]=d[1]&&b?b(d[0],d[1]):d[1],i+="<div "+f(a,e.cssClasses.marker,d)+"></div>",d[1]&&(i+="<div "+f(a,e.cssClasses.value,d)+">"+c.to(d[0])+"</div>")}var h=document.createElement("div"),i="",k=[e.cssClasses.valueNormal,e.cssClasses.valueLarge,e.cssClasses.valueSub],l=[e.cssClasses.markerNormal,e.cssClasses.markerLarge,e.cssClasses.markerSub],m=[e.cssClasses.valueHorizontal,e.cssClasses.valueVertical],n=[e.cssClasses.markerHorizontal,e.cssClasses.markerVertical];return j(h,e.cssClasses.pips),j(h,0===e.ort?e.cssClasses.pipsHorizontal:e.cssClasses.pipsVertical),Object.keys(a).forEach(function(b){g(b,a[b])}),h.innerHTML=i,h}function x(a){var b=a.mode,c=a.density||1,d=a.filter||!1,e=a.values||!1,f=a.stepped||!1,g=u(b,e,f),h=v(c,b,g),i=a.format||{to:Math.round};return ga.appendChild(w(h,d,i))}function y(){var a=ba.getBoundingClientRect(),b="offset"+["Width","Height"][e.ort];return 0===e.ort?a.width||ba[b]:a.height||ba[b]}function z(a,b,c,d){var f=function(b){return!ga.hasAttribute("disabled")&&(!l(ga,e.cssClasses.tap)&&(!!(b=A(b,d.pageOffset))&&(!(a===fa.start&&void 0!==b.buttons&&b.buttons>1)&&((!d.hover||!b.buttons)&&(b.calcPoint=b.points[e.ort],void c(b,d))))))},g=[];return a.split(" ").forEach(function(a){b.addEventListener(a,f,!1),g.push([a,f])}),g}function A(a,b){a.preventDefault();var c,d,e=0===a.type.indexOf("touch"),f=0===a.type.indexOf("mouse"),g=0===a.type.indexOf("pointer");if(0===a.type.indexOf("MSPointer")&&(g=!0),e){if(a.touches.length>1)return!1;c=a.changedTouches[0].pageX,d=a.changedTouches[0].pageY}return b=b||m(),(f||g)&&(c=a.clientX+b.x,d=a.clientY+b.y),a.pageOffset=b,a.points=[c,d],a.cursor=f||g,a}function B(a){var b=a-d(ba,e.ort),c=100*b/y();return e.dir?100-c:c}function C(a){var b=100,c=!1;return ca.forEach(function(d,e){if(!d.hasAttribute("disabled")){var f=Math.abs(ha[e]-a);f<b&&(c=e,b=f)}}),c}function D(a,b,c,d){var e=c.slice(),f=[!a,a],g=[a,!a];d=d.slice(),a&&d.reverse(),d.length>1?d.forEach(function(a,c){var d=M(e,a,e[a]+b,f[c],g[c]);d===!1?b=0:(b=d-e[a],e[a]=d)}):f=g=[!0];var h=!1;d.forEach(function(a,d){h=Q(a,c[a]+b,f[d],g[d])||h}),h&&d.forEach(function(a){E("update",a),E("slide",a)})}function E(a,b,c){Object.keys(ma).forEach(function(d){var f=d.split(".")[0];a===f&&ma[d].forEach(function(a){a.call(ea,la.map(e.format.to),b,la.slice(),c||!1,ha.slice())})})}function F(a,b){"mouseout"===a.type&&"HTML"===a.target.nodeName&&null===a.relatedTarget&&H(a,b)}function G(a,b){if(navigator.appVersion.indexOf("MSIE 9")===-1&&0===a.buttons&&0!==b.buttonsProperty)return H(a,b);var c=(e.dir?-1:1)*(a.calcPoint-b.startCalcPoint),d=100*c/b.baseSize;D(c>0,d,b.locations,b.handleNumbers)}function H(a,b){ja&&(k(ja,e.cssClasses.active),ja=!1),a.cursor&&(document.body.style.cursor="",document.body.removeEventListener("selectstart",document.body.noUiListener)),document.documentElement.noUiListeners.forEach(function(a){document.documentElement.removeEventListener(a[0],a[1])}),k(ga,e.cssClasses.drag),P(),b.handleNumbers.forEach(function(a){E("set",a),E("change",a),E("end",a)})}function I(a,b){if(1===b.handleNumbers.length){var c=ca[b.handleNumbers[0]];if(c.hasAttribute("disabled"))return!1;ja=c.children[0],j(ja,e.cssClasses.active)}a.preventDefault(),a.stopPropagation();var d=z(fa.move,document.documentElement,G,{startCalcPoint:a.calcPoint,baseSize:y(),pageOffset:a.pageOffset,handleNumbers:b.handleNumbers,buttonsProperty:a.buttons,locations:ha.slice()}),f=z(fa.end,document.documentElement,H,{handleNumbers:b.handleNumbers}),g=z("mouseout",document.documentElement,F,{handleNumbers:b.handleNumbers});if(document.documentElement.noUiListeners=d.concat(f,g),a.cursor){document.body.style.cursor=getComputedStyle(a.target).cursor,ca.length>1&&j(ga,e.cssClasses.drag);var h=function(){return!1};document.body.noUiListener=h,document.body.addEventListener("selectstart",h,!1)}b.handleNumbers.forEach(function(a){E("start",a)})}function J(a){a.stopPropagation();var b=B(a.calcPoint),c=C(b);return c!==!1&&(e.events.snap||f(ga,e.cssClasses.tap,e.animationDuration),Q(c,b,!0,!0),P(),E("slide",c,!0),E("set",c,!0),E("change",c,!0),E("update",c,!0),void(e.events.snap&&I(a,{handleNumbers:[c]})))}function K(a){var b=B(a.calcPoint),c=ka.getStep(b),d=ka.fromStepping(c);Object.keys(ma).forEach(function(a){"hover"===a.split(".")[0]&&ma[a].forEach(function(a){a.call(ea,d)})})}function L(a){a.fixed||ca.forEach(function(a,b){z(fa.start,a.children[0],I,{handleNumbers:[b]})}),a.tap&&z(fa.start,ba,J,{}),a.hover&&z(fa.move,ba,K,{hover:!0}),a.drag&&da.forEach(function(b,c){if(b!==!1&&0!==c&&c!==da.length-1){var d=ca[c-1],f=ca[c],g=[b];j(b,e.cssClasses.draggable),a.fixed&&(g.push(d.children[0]),g.push(f.children[0])),g.forEach(function(a){z(fa.start,a,I,{handles:[d,f],handleNumbers:[c-1,c]})})}})}function M(a,b,c,d,f){return ca.length>1&&(d&&b>0&&(c=Math.max(c,a[b-1]+e.margin)),f&&b<ca.length-1&&(c=Math.min(c,a[b+1]-e.margin))),ca.length>1&&e.limit&&(d&&b>0&&(c=Math.min(c,a[b-1]+e.limit)),f&&b<ca.length-1&&(c=Math.max(c,a[b+1]-e.limit))),e.padding&&(0===b&&(c=Math.max(c,e.padding)),b===ca.length-1&&(c=Math.min(c,100-e.padding))),c=ka.getStep(c),c=g(c),c!==a[b]&&c}function N(a){return a+"%"}function O(a,b){ha[a]=b,la[a]=ka.fromStepping(b);var c=function(){ca[a].style[e.style]=N(b),S(a),S(a+1)};window.requestAnimationFrame&&e.useRequestAnimationFrame?window.requestAnimationFrame(c):c()}function P(){ia.forEach(function(a){var b=ha[a]>50?-1:1,c=3+(ca.length+b*a);ca[a].childNodes[0].style.zIndex=c})}function Q(a,b,c,d){return b=M(ha,a,b,c,d),b!==!1&&(O(a,b),!0)}function S(a){if(da[a]){var b=0,c=100;0!==a&&(b=ha[a-1]),a!==da.length-1&&(c=ha[a]),da[a].style[e.style]=N(b),da[a].style[e.styleOposite]=N(100-c)}}function T(a,b){null!==a&&a!==!1&&("number"==typeof a&&(a=String(a)),a=e.format.from(a),a===!1||isNaN(a)||Q(b,ka.toStepping(a),!1,!1))}function V(a,b){var c=h(a),d=void 0===ha[0];b=void 0===b||!!b,c.forEach(T),e.animate&&!d&&f(ga,e.cssClasses.tap,e.animationDuration),ia.forEach(function(a){Q(a,ha[a],!0,!1)}),P(),ia.forEach(function(a){E("update",a),null!==c[a]&&b&&E("set",a)})}function W(a){V(e.start,a)}function X(){var a=la.map(e.format.to);return 1===a.length?a[0]:a}function Y(){for(var a in e.cssClasses)e.cssClasses.hasOwnProperty(a)&&k(ga,e.cssClasses[a]);for(;ga.firstChild;)ga.removeChild(ga.firstChild);delete ga.noUiSlider}function Z(){return ha.map(function(a,b){var c=ka.getNearbySteps(a),d=la[b],e=c.thisStep.step,f=null;e!==!1&&d+e>c.stepAfter.startValue&&(e=c.stepAfter.startValue-d),f=d>c.thisStep.startValue?c.thisStep.step:c.stepBefore.step!==!1&&d-c.stepBefore.highestStep,100===a?e=null:0===a&&(f=null);var g=ka.countStepDecimals();return null!==e&&e!==!1&&(e=Number(e.toFixed(g))),null!==f&&f!==!1&&(f=Number(f.toFixed(g))),[f,e]})}function $(a,b){ma[a]=ma[a]||[],ma[a].push(b),"update"===a.split(".")[0]&&ca.forEach(function(a,b){E("update",b)})}function _(a){var b=a&&a.split(".")[0],c=b&&a.substring(b.length);Object.keys(ma).forEach(function(a){var d=a.split(".")[0],e=a.substring(d.length);b&&b!==d||c&&c!==e||delete ma[a]})}function aa(a,b){var c=X(),d=["margin","limit","padding","range","animate","snap","step","format"];d.forEach(function(b){void 0!==a[b]&&(i[b]=a[b])});var f=R(i);d.forEach(function(b){void 0!==a[b]&&(e[b]=f[b])}),f.spectrum.direction=ka.direction,ka=f.spectrum,e.margin=f.margin,e.limit=f.limit,e.padding=f.padding,ha=[],V(a.start||c,b)}var ba,ca,da,ea,fa=n(),ga=c,ha=[],ia=[],ja=!1,ka=e.spectrum,la=[],ma={};if(ga.noUiSlider)throw new Error("noUiSlider ("+U+"): Slider was already initialized.");return r(ga),q(e.connect,ba),ea={destroy:Y,steps:Z,on:$,off:_,get:X,set:V,reset:W,__moveHandles:function(a,b,c){D(a,b,ha,c)},options:i,updateOptions:aa,target:ga,pips:x},L(e.events),V(e.start),e.pips&&x(e.pips),e.tooltips&&t(),ea}function T(a,b){if(!a.nodeName)throw new Error("noUiSlider ("+U+"): create requires a single element.");var c=R(b,a),d=S(a,c,b);return a.noUiSlider=d,d}var U="9.2.0";y.prototype.getMargin=function(a){var b=this.xNumSteps[0];if(b&&a/b%1!==0)throw new Error("noUiSlider ("+U+"): 'limit', 'margin' and 'padding' must be divisible by step.");return 2===this.xPct.length&&p(this.xVal,a)},y.prototype.toStepping=function(a){return a=t(this.xVal,this.xPct,a)},y.prototype.fromStepping=function(a){return u(this.xVal,this.xPct,a)},y.prototype.getStep=function(a){return a=v(this.xPct,this.xSteps,this.snap,a)},y.prototype.getNearbySteps=function(a){var b=s(a,this.xPct);return{stepBefore:{startValue:this.xVal[b-2],step:this.xNumSteps[b-2],highestStep:this.xHighestCompleteStep[b-2]},thisStep:{startValue:this.xVal[b-1],step:this.xNumSteps[b-1],highestStep:this.xHighestCompleteStep[b-1]},stepAfter:{startValue:this.xVal[b-0],step:this.xNumSteps[b-0],highestStep:this.xHighestCompleteStep[b-0]}}},y.prototype.countStepDecimals=function(){var a=this.xNumSteps.map(i);return Math.max.apply(null,a)},y.prototype.convert=function(a){return this.getStep(this.toStepping(a))};var V={to:function(a){return void 0!==a&&a.toFixed(2)},from:Number};return{version:U,create:T}});
    </script> 
  </body>
</html>
<script>
  const AUDIO_CONTEXT = new AudioContext();
  const ANALYSER = AUDIO_CONTEXT.createAnalyser();
  //	**************	Settings stuff	**************
  //	Selected visualization style. This will determine which visualization function to run/stop
  var selected = '';

  //	"Frequency Bars" settings variables
  var freq_bars_sliders;
  var freq_bars_values;
  var freq_bars_checkboxes;

  //	"Windmill" settings variables
  var windmill_sliders;
  var windmill_sliders_values;
  var windmill_checkboxes

  //	FPS counter for testing
  var lastLoop = (new Date()).getMilliseconds();
  var fpsCounter = 1;
  var fps = 0;
  var showFPS = function(){
    var currentLoop = (new Date()).getMilliseconds();
    if(lastLoop > currentLoop){
      fps = fpsCounter;
      fpsCounter = 1;
    }
    else{
      fpsCounter += 1;
    }
    lastLoop = currentLoop;
    console.log(fps);
  }

  var WIDTH, HEIGHT;

  //	Entry point to the whole app
  window.onload = function init() {
    //	Use sound card's "Stereo Mix" as the audio source, then connect it to ANALYSER
    //	so we can extract frequency data from it to visualize
    navigator.mediaDevices.getUserMedia({audio: true, video: false}).then(function(stream){
      var source = AUDIO_CONTEXT.createMediaStreamSource(stream);
      source.connect(ANALYSER);
    }).catch(function(err){
      console.log(err.name + ": " + err.message)
    });
    //	Initializes the Sliding Menu by adding an event listener to the button
    initMenu();
    //	Initializes the Frequency Bars settings with event listeners and sliders
    initFreqBarsStyleSettings();
    //	Initializes the Windmill settings the same way as above
    initWindmillStyleSettings();
    //	Initializes the Style Chooser with event listeners
    initVizStyleChooser();
  }

  //	**************	Menu stuff	**************
  function initMenu(){
    //	DOM Elements
    const SETTINGS_BUTTON = document.getElementById('settings-button');
    const SIDE_MENU = document.getElementById('side-menu');
    //	Toggle menu open/close
    var open = false
    SETTINGS_BUTTON.addEventListener('click', function(){
      if(open == false){
        open = true;
        SETTINGS_BUTTON.style.transform = 'translate(506px, 0px)';
        SETTINGS_BUTTON.className = 'fa fa-arrow-left fa-2x';
        SIDE_MENU.style.transform = 'translateX(0px)';
      }
      else{
        open = false;
        SETTINGS_BUTTON.style.transform = 'translate(0px, 0px)';
        SETTINGS_BUTTON.className = 'fa fa-arrow-right fa-2x';
        SIDE_MENU.style.transform = 'translateX(-510px)';
      }
    });
  }

  //	**************	Visualization style selection	**************
  function initVizStyleChooser(){
    const STYLES = document.getElementsByClassName('viz-style');
    const STYLE_SETTINGS_MENU = document.getElementsByClassName('viz-settings-visibility');

    for(let i=0; i<STYLES.length; i++){
      STYLES[i].addEventListener('click', function(){
        //	Clear any existing canvas
        var toClear = document.getElementsByTagName('canvas');
        for(let i=0; i<toClear.length; i++){
          toClear[i].remove();
        }

        //	Deselect all the other Styles
        for(let j=0; j < STYLES.length; j++){
          STYLES[j].className = 'viz-style generic-menu-item';
          STYLE_SETTINGS_MENU[j].style = "display: none;"
        }

        STYLES[i].className = 'viz-style generic-menu-item selected';
        selected = STYLES[i].innerHTML;

        switch(i){
            //	Windmill
          case 0:
            STYLE_SETTINGS_MENU[i].style = "display: block;"
            visualizeWindmill();
            break;
            //	Frequency Bars
          case 1:
            STYLE_SETTINGS_MENU[i].style = "display: block;"
            visualizeFrequencyBars();
            break;
          case 2:
            visualizeNew();
            break;
        }
      });
    }
    //	"Windmill" is the default style when the app starts
    STYLES[0].click();
  }

  //	**************	"Windmill" Style Settings 	**************
  function initWindmillStyleSettings(){
    windmill_sliders = document.getElementsByClassName('windmill-slider');
    windmill_sliders_values = document.getElementsByClassName('windmill-slider-value');
    windmill_checkboxes = document.getElementsByClassName('toggle-windmill');
    const WINDMILL_PRESETS = document.getElementsByClassName('windmill-presets');

    function updateSliderDisplayValue(){

      for(let i=0; i<windmill_sliders.length; i++){
        if(typeof windmill_sliders[i].noUiSlider != 'undefined'){
          if(i === 3 || i === 7 || i === 8 || i === 12 || i === 13){
            windmill_sliders_values[i].innerHTML = windmill_sliders[i].noUiSlider.get();
          }
          else{
            windmill_sliders_values[i].innerHTML = Math.round(windmill_sliders[i].noUiSlider.get());
          }
        }
      }
    }

    function createSliders(){

      for(let i=0; i<windmill_sliders.length;i++){
        //	Alphas
        if(i === 3 || i === 7 || i === 12 ){
          noUiSlider.create(windmill_sliders[i],{
            start: 1,
            step: 0.01,
            range: {
              'min': 0,
              'max': 1.0
            },
            connect: [true, false]
          });
        }
        //	Chaos slider
        else if(i === 13){
          noUiSlider.create(windmill_sliders[i],{
            start: 0,
            step: 0.01,
            range: {
              'min': 0,
              'max': 3.5
            },
            connect: [true, false]
          });
        }
        //	Blade Width
        else if(i === 8){
          noUiSlider.create(windmill_sliders[i],{
            start: 0.5,
            step: 0.1,
            range: {
              'min': 0.2,
              'max': 5.0
            },
            connect: [true, false]
          });
        }
        else{
          noUiSlider.create(windmill_sliders[i],{
            start: 120,
            step: 1,
            range: {
              'min': 0,
              'max': 255
            },
            connect: [true, false]
          });
        }
        windmill_sliders[i].noUiSlider.on('update', updateSliderDisplayValue);
      }
    }

    function initPresets(){

      for(let i=0; i<WINDMILL_PRESETS.length; i++){
        WINDMILL_PRESETS[i].addEventListener('click', function(){
          //	Deselect all the presets, then select the one that was clicked
          for(let j=0; j<WINDMILL_PRESETS.length; j++){
            WINDMILL_PRESETS[j].className = "windmill-presets generic-menu-item";
          }
          WINDMILL_PRESETS[i].className = "windmill-presets generic-menu-item selected";
          let presetSliderSettings;
          switch(i){
              //	Default
            case 0:
              presetSliderSettings = [120,120,120,1, 120,120,120,1, 0.2, 120,120,120,1, 1.1];
              for(let k=0; k<windmill_sliders.length; k++){
                let presetValue = presetSliderSettings[k];
                windmill_sliders[k].noUiSlider.set(presetValue);
              }
              windmill_checkboxes[0].checked = true;
              break;
          }
        });
      }
    }

    createSliders();

    initPresets();

    //	Manually default to this preset
    WINDMILL_PRESETS[0].click();
  }

  function visualizeWindmill(){
    //	Create a new Canvas element and insert it into the DOM
    var canvasElement = document.createElement('canvas')
    canvasElement.setAttribute('id', 's');
    document.body.appendChild(canvasElement);
    canvasCtx = document.getElementById('s').getContext('2d');

    var rotation = 0;

    ANALYSER.fftSize = 512;

    var bufferLength = ANALYSER.frequencyBinCount;
    var dataArray = new Uint8Array(bufferLength);

    var grd;
    var radius, arcStart, arcEnd, WIDTH, HEIGHT;
    var expand;

    var background1_r, background1_g, background1_b, background1_a,
        background2_r, background2_g, background2_b, background2_a;

    var useRainbowBlades;
    var bladeStyle1, bladeStyle2;

    var chaos;

    function readSliders(){
      //	Get the color values from the slider settings
      //	Background 1 RGBA colors
      background1_r = Math.round(windmill_sliders[0].noUiSlider.get());
      background1_g = Math.round(windmill_sliders[1].noUiSlider.get());
      background1_b = Math.round(windmill_sliders[2].noUiSlider.get());
      background1_a = windmill_sliders[3].noUiSlider.get();

      //	Background 2 RGBA colors
      background2_r = Math.round(windmill_sliders[4].noUiSlider.get());
      background2_g = Math.round(windmill_sliders[5].noUiSlider.get());
      background2_b = Math.round(windmill_sliders[6].noUiSlider.get());
      background2_a = windmill_sliders[7].noUiSlider.get();

      //	Blade RGBA colors
      blade_r = Math.round(windmill_sliders[9].noUiSlider.get());
      blade_g = Math.round(windmill_sliders[10].noUiSlider.get());
      blade_b = Math.round(windmill_sliders[11].noUiSlider.get());
      blade_a = windmill_sliders[12].noUiSlider.get();

      chaos = windmill_sliders[13].noUiSlider.get();

      bladeWidth = windmill_sliders[8].noUiSlider.get();

      if(windmill_checkboxes[0].checked === false){
        document.getElementById('hidden-windmill-sliders').style = 'display: block;'
        useRainbowBlades = false;
      }
      else{
        document.getElementById('hidden-windmill-sliders').style = 'display: none;'
        useRainbowBlades = true;
      }
    }

    function drawWindmillBlades(){
      for(let i=1; i< 50; i+= 1){
        if(useRainbowBlades){
          bladeStyle1 = 'hsl(' + (360-(i*10)) + ',100%, 50%)';
          bladeStyle2 = 'hsl(' + (i*10) + ',100%, 50%)';
        }
        else{
          bladeStyle1 = 'rgba(' + blade_r + ',' + blade_g + ',' + blade_b + ',' + blade_a + ')';
          bladeStyle2 = 'rgba(' + blade_r + ',' + blade_g + ',' + blade_b + ',' + blade_a + ')';
        }
        radius = Math.round(20 + (Math.pow(i, 1.8))) + dataArray[i]*chaos;
        arcStart = (i/24) + rotation;
        arcEnd = (i/24) + rotation + Math.pow(dataArray[i*2]/200, 0.8);

        for(let j=1; j<7; j++){
          //	First "blade"
          canvasCtx.beginPath();
          canvasCtx.lineCap ='round';
          canvasCtx.strokeStyle = bladeStyle1;
          canvasCtx.arc(WIDTH/2, HEIGHT/2, radius + (j*bladeWidth), arcStart, arcEnd);
          canvasCtx.stroke();

          //	Second blade
          canvasCtx.beginPath();
          canvasCtx.lineCap ='round';
          canvasCtx.strokeStyle = bladeStyle2;
          canvasCtx.arc(WIDTH/2, HEIGHT/2, radius + (j*bladeWidth), arcStart + (Math.PI*2/4), arcEnd + (Math.PI*2/4));
          canvasCtx.stroke();

          //	Third Blade
          canvasCtx.beginPath();
          canvasCtx.lineCap ='round';
          canvasCtx.strokeStyle = bladeStyle1;
          canvasCtx.arc(WIDTH/2, HEIGHT/2, radius + (j*bladeWidth), arcStart + (Math.PI*2/4*2), arcEnd + (Math.PI*2/4*2));
          canvasCtx.stroke();

          //	Fourth Blade
          canvasCtx.beginPath();
          canvasCtx.lineCap ='round';
          canvasCtx.strokeStyle = bladeStyle2;
          canvasCtx.arc(WIDTH/2, HEIGHT/2, radius + (j*bladeWidth), arcStart + (Math.PI*2/4*3), arcEnd + (Math.PI*2/4*3));
          canvasCtx.stroke();
        }
      }
    }

    function drawSpiralRings(){
      expand = dataArray[45]*1.2;
      //	Black hole
      canvasCtx.beginPath();
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+60, 0, 2 * Math.PI);
      canvasCtx.fillStyle = 'rgba(0,0,0,0.8)';
      canvasCtx.fill();

      //	White arc 1
      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(255, 255, 255, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+65, Math.PI - rotation, Math.PI + 2 - rotation);
      canvasCtx.lineWidth = 4;
      canvasCtx.stroke();

      //	White arc 2
      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(255, 255, 255, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+65, (Math.PI+2)+Math.PI - rotation, Math.PI*2 - rotation, true);
      //canvasCtx.lineWidth = 4;
      canvasCtx.stroke();

      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(0, 255, 100, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+250, 0 - rotation, 0.5 * Math.PI - rotation);
      //canvasCtx.lineWidth = 6;
      canvasCtx.stroke();

      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(150, 20, 100, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+250, 0.5 * Math.PI - rotation, Math.PI + 1 - rotation);
      canvasCtx.stroke();

      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(20, 20, 185, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+250, Math.PI+1 - rotation, 0 - rotation);
      canvasCtx.stroke();

      // White arc 3
      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(255, 255, 255, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+430, Math.PI - rotation, Math.PI + 2 - rotation);
      //canvasCtx.lineWidth = 4;
      canvasCtx.stroke();

      //	White arc 4
      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(255, 255, 255, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+430, (Math.PI+2)+Math.PI - rotation, Math.PI*2 - rotation, true);
      //canvasCtx.lineWidth = 4;
      canvasCtx.stroke();

      //	Tricolor circle 2
      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(0, 255, 100, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+620, 0 - rotation, 0.5 * Math.PI - rotation);
      //canvasCtx.lineWidth = 6;
      canvasCtx.stroke();

      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(150, 20, 100, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+620, 0.5 * Math.PI - rotation, Math.PI + 1 - rotation);
      canvasCtx.stroke();

      canvasCtx.beginPath();
      canvasCtx.strokeStyle = 'rgba(20, 20, 185, 1.0)';
      canvasCtx.arc(WIDTH/2, HEIGHT/2, expand+620, Math.PI+1 - rotation, 0 - rotation);
      canvasCtx.stroke();
    }

    function draw() {
      //	Count FPS
      showFPS();

      readSliders();

      //	Resize the canvas every frame to match the window size
      canvasCtx.canvas.width = WIDTH = window.innerWidth;
      canvasCtx.canvas.height = HEIGHT = window.innerHeight;

      //	Check if this is still the selected visualization style
      if(selected === 'Windmill'){
        requestAnimationFrame(draw);
      }
      //	Fills 'dataArray' with frequency data from the audio source.
      ANALYSER.getByteFrequencyData(dataArray);

      grd = canvasCtx.createLinearGradient(0, 0, 170, HEIGHT);
      //	Color the background
      grd.addColorStop(0, 'rgba(5, 5, 15, 1.0)');
      grd.addColorStop(1, 'rgba(5, 10, 25, 1.0)');
      //	Apply the gradient to the next rectangle to be drawn, then set it as the background
      canvasCtx.fillStyle = grd;
      canvasCtx.fillRect(0, 0, WIDTH, HEIGHT);

      rotation += dataArray[15]/8000;
      if(rotation < 2*Math.PI){
        rotation += (Math.PI/4000);
      }
      else{
        rotation = 0;
      }

      drawWindmillBlades();

      drawSpiralRings();

    }
    draw();
  }

  //	**************	"Frequency Bars" Style Settings 	**************
  function initFreqBarsStyleSettings(){
    //	All the "Frequency Bars" settings sliders
    freq_bars_sliders = document.getElementsByClassName('freq-bars-slider');
    freq_bars_values = document.getElementsByClassName('freq-bars-slider-value');
    //	Automation Checkboxes
    freq_bars_checkboxes = document.getElementsByClassName('freq-bars-responsive');
    const BARS_PRESETS = document.getElementsByClassName('bars-presets');

    //	Callback function in response to a slider's update' events. 
    //	This function updates the display value on the page to reflect the value of the slider 
    function updateSliderDisplayValue(){
      for(let i=0; i<freq_bars_sliders.length; i++){
        if(typeof freq_bars_sliders[i].noUiSlider != 'undefined'){
          if(i === 3 || i === 7 || i === 11 || i === 13){
            freq_bars_values[i].innerHTML = freq_bars_sliders[i].noUiSlider.get();
          }
          else if(i === 12){
            freq_bars_values[i].innerHTML = Math.pow(2, Math.round(freq_bars_sliders[i].noUiSlider.get()))/2;
          }
          else{
            freq_bars_values[i].innerHTML = Math.round(freq_bars_sliders[i].noUiSlider.get());
          }
        }
      }
    }

    function createSliders(){
      /*
			Initializes an array to hold all the sliders for "Frequency Bars".
			Uses noUiSlider's constructor to create mulitple sliders.
			freq_bars_sliders[0] = BG1 Red
			freq_bars_sliders[1] = BG1 Green
			freq_bars_sliders[2] = BG1 Blue
			freq_bars_sliders[3] = BG1 Alpha
			freq_bars_sliders[4] = BG2 Red
			freq_bars_sliders[5] = BG2 Green
			freq_bars_sliders[6] = BG2 Blue
			freq_bars_sliders[7] = BG2 Alpha
			...etc
		*/
      for(let i = 0; i < freq_bars_sliders.length; i++){
        //	i=3, i=7, and i=11 are opacity sliders. They have a different scale
        if(i === 3 || i === 7 || i === 11){
          noUiSlider.create(freq_bars_sliders[i],{
            start: 1.0,
            step: 0.01,
            range: {
              'min': 0,
              'max': 1.0
            },
            connect: [true, false]
          });
        }
        //	i=12 is the BAR COUNT slider.
        else if(i === 12){
          noUiSlider.create(freq_bars_sliders[i],{
            start: 9,
            step: 1,
            range: {
              'min': 5,
              'max': 13
            },
            connect: [true, false]
          });
        }
        else if(i === 13){
          noUiSlider.create(freq_bars_sliders[i],{
            start: 0.6,
            step: 0.01,
            range: {
              'min': 0.0,
              'max': 1.0
            },
            connect: [true, false]
          });
        }
        //	RGB Sliders
        else{
          noUiSlider.create(freq_bars_sliders[i],{
            start: 120,
            step: 1,
            range: {
              'min': 0,
              'max': 255
            },
            connect: [true, false]
          });
        }
        //	Bind callback function to the 'update' event for this particular slider
        freq_bars_sliders[i].noUiSlider.on('update', updateSliderDisplayValue);
      }
    }

    //	**************PRESET STYLE SELECTION**************
    //	Store all the preset choices into an array so we can programatically add
    //	event listeners to each.
    function initPresets(){

      for(let i=0; i<BARS_PRESETS.length; i++){
        BARS_PRESETS[i].addEventListener('click', function(){
          //	Deselect all the presets, then select the one that was clicked
          for(let j=0; j<BARS_PRESETS.length; j++){
            BARS_PRESETS[j].className = "bars-presets generic-menu-item";
          }
          BARS_PRESETS[i].className = "bars-presets generic-menu-item selected";
          let presetSliderSettings;
          switch(i){
              //	Blue Sky
            case 0:
              presetSliderSettings = [100, 200, 230, 1.0, 102, 102, 255, 0.5, 85, 100, 250, 1.0, 8, 0.40];
              for(let k=0; k<freq_bars_sliders.length; k++){
                let presetValue = presetSliderSettings[k];
                freq_bars_sliders[k].noUiSlider.set(presetValue);
              }
              freq_bars_checkboxes[0].checked = true;
              freq_bars_checkboxes[1].checked = false;
              freq_bars_checkboxes[2].checked = false;
              break;
              //	Neon Purple
            case 1:
              presetSliderSettings = [255, 74, 243, 1.0, 0, 17, 20, 0.63, 55, 227, 101, 1.0, 8, 0.45];
              for(let k=0; k<freq_bars_sliders.length; k++){
                let presetValue = presetSliderSettings[k];
                freq_bars_sliders[k].noUiSlider.set(presetValue);
              }
              freq_bars_checkboxes[0].checked = true;
              freq_bars_checkboxes[1].checked = false;
              freq_bars_checkboxes[2].checked = false;
              break;
              //	Twilight
            case 2:
              presetSliderSettings = [0, 0, 49, 1.0, 19, 0, 0, 0.85, 51, 8, 206, 0.32, 9, 0.40];
              for(let k=0; k<freq_bars_sliders.length; k++){
                let presetValue = presetSliderSettings[k];
                freq_bars_sliders[k].noUiSlider.set(presetValue);
              }
              freq_bars_checkboxes[0].checked = false;
              freq_bars_checkboxes[1].checked = true;
              freq_bars_checkboxes[2].checked = true;
              break;
              //	Chill vibes
            case 3:
              presetSliderSettings = [238, 90, 20, 0.56, 255, 74, 243, 1.0, 54, 198, 185, 0.68, 9, 0.42];
              for(let k=0; k<freq_bars_sliders.length; k++){
                let presetValue = presetSliderSettings[k];
                freq_bars_sliders[k].noUiSlider.set(presetValue);
              }
              freq_bars_checkboxes[0].checked = false;
              freq_bars_checkboxes[1].checked = true;
              freq_bars_checkboxes[2].checked = false;
              break;
          }
        });
      }
    }

    createSliders();

    initPresets();

    //	Manually default to this preset
    BARS_PRESETS[0].click();
  }

  function visualizeFrequencyBars(){
    //	Create a new Canvas element and insert it into the DOM
    var canvasElement = document.createElement('canvas')
    canvasElement.setAttribute('id', 'c');
    document.body.appendChild(canvasElement);
    var canvasCtx = document.getElementById('c').getContext('2d');

    //	Declare variables here to avoid garbage collection in the draw() loop for better performance
    var bar_count;
    var bufferLength;
    var dataArray;
    var grd;
    var background1_r, background1_g, background1_b, background1_a,
        background2_r, background2_g, background2_b, background2_a,
        barColor_r, barColor_g, barColor_b, barColor_a,
        barHeight_setting;
    var responsiveBarColor_r = responsiveBarColor_g = responsiveBarColor_b = 0;
    var barWidth, barHeight, x;

    function readSliders(){
      //	Read the value from the appropriate settings slider
      bar_count = Math.pow(2, Math.round(freq_bars_sliders[12].noUiSlider.get()));

      //	Get the color values from the slider settings
      //	Background 1 RGBA colors
      background1_r = Math.round(freq_bars_sliders[0].noUiSlider.get());
      background1_g = Math.round(freq_bars_sliders[1].noUiSlider.get());
      background1_b = Math.round(freq_bars_sliders[2].noUiSlider.get());
      background1_a = freq_bars_sliders[3].noUiSlider.get();

      //	Background 2 RGBA colors
      background2_r = Math.round(freq_bars_sliders[4].noUiSlider.get());
      background2_g = Math.round(freq_bars_sliders[5].noUiSlider.get());
      background2_b = Math.round(freq_bars_sliders[6].noUiSlider.get());
      background2_a = freq_bars_sliders[7].noUiSlider.get();

      //	Bar Color RGBA colors
      barColor_r = Math.round(freq_bars_sliders[8].noUiSlider.get());
      barColor_g = Math.round(freq_bars_sliders[9].noUiSlider.get());
      barColor_b = Math.round(freq_bars_sliders[10].noUiSlider.get());
      barColor_a = freq_bars_sliders[11].noUiSlider.get();

      //	Bar Height slider
      barHeight_setting = freq_bars_sliders[13].noUiSlider.get();

      //	Responsive Bar Colors
      if(freq_bars_checkboxes[0].checked === true){
        responsiveBarColor_r = 1;
      }
      else{
        responsiveBarColor_r = 0;
      }
      if(freq_bars_checkboxes[1].checked === true){
        responsiveBarColor_g = 1;
      }
      else{
        responsiveBarColor_g = 0;
      }
      if(freq_bars_checkboxes[2].checked === true){
        responsiveBarColor_b = 1;
      }
      else{
        responsiveBarColor_b = 0;
      }
    }

    //	The 'meat' of this whole function :)
    function draw() {
      showFPS();

      //	Resize the canvas every frame to match the window size
      canvasCtx.canvas.width = WIDTH = window.innerWidth;
      canvasCtx.canvas.height = HEIGHT = window.innerHeight;
      //	Check if this is still the selected visualization style
      if(selected === 'Frequency Bars'){
        requestAnimationFrame(draw);
      }

      //	Get all the slider values before we render the visualizations
      readSliders();

      //	Max size: 32768
      //	Must be a power of 2
      ANALYSER.fftSize = bar_count;
      /*
		 *	The frequency bin count is always half of fftSize.
		 *	Since the frequency bands are split evenly, each element
		 *	N in dataArray will correspond to:
		 *	N * sampleRate / fftSize
		 *
		 *	Note that the Audio Context defaults to sampleRate = 48000
		 */
      bufferLength = ANALYSER.frequencyBinCount;
      dataArray = new Uint8Array(bufferLength);
      //	Fills 'dataArray' with frequency data from the audio source.
      ANALYSER.getByteFrequencyData(dataArray);


      // Initialize the gradient color for the background
      grd = canvasCtx.createLinearGradient(0, 0, 170, HEIGHT);
      //	Color the background
      grd.addColorStop(0, 'rgba('+ background1_r +', '+ background1_g +', '+ background1_b +', '+ background1_a +')');
      grd.addColorStop(1, 'rgba('+ background2_r +', '+ background2_g +', '+ background2_b +', '+ background2_a +')');
      canvasCtx.fillStyle = grd;
      canvasCtx.fillRect(0, 0, WIDTH, HEIGHT);

      //	Draw the bars
      barWidth = (WIDTH / bufferLength);
      x = 0;
      for(let i = 0; i < bufferLength; i++){
        //	RGB needs to take integers, so we need to round 'barHeight'.
        barHeight = Math.round(barHeight_setting * (Math.max(((dataArray[i] * 4) - 250), 0)))+10;
        canvasCtx.fillStyle = 'rgba(' + ((dataArray[i]*responsiveBarColor_r) + barColor_r) + ','+ ((dataArray[i]*responsiveBarColor_g) + barColor_g) +', '+ ((dataArray[i]*responsiveBarColor_b) + barColor_b) +', '+ barColor_a +')';
        canvasCtx.fillRect(x,HEIGHT-barHeight/2-HEIGHT/2, barWidth, barHeight);
        x += barWidth + 1;
      }

      //canvasCtx.rotate(dataArray[25]/180);
    }
    draw();
  }

  /*
function visualizeWaveform(){
	//	Create a new Canvas element and insert it into the DOM
	var canvasElement = document.createElement('canvas')
	canvasElement.setAttribute('id', 'c');
	document.body.appendChild(canvasElement);
	canvasCtx = document.getElementById('c').getContext('2d');
	var stars = [];
	//	Create stars
	for(let i=0; i< 20; i++){
 		stars.push(new Star());
 	}
	function Star(){
		this.active = false;
	}
	Star.prototype.createStar = function(){
		this.x = WIDTH / 2;
		this.y = HEIGHT / 2;
		this.length = 1;
		this.vx = (Math.random() * 10 - 5)*5;
		this.vy = (Math.random() * 10 - 5)*5;
		this.gravity = 0.0;
		this.active = true;
		canvasCtx.beginPath();
			canvasCtx.moveTo(this.x + (Math.random() * 10)*2, this.y + (Math.random() * 10)*2)
			canvasCtx.lineTo(this.x+this.vx, this.y + this.vy)
		canvasCtx.strokeStyle = 'rgb(255,255,255)';
		canvasCtx.stroke();
	}
	Star.prototype.moveStar = function(){
		this.active = true;
		this.x += this.vx;
		this.y += this.vy;
		this.vy += this.gravity;
		this.length = Math.abs(this.length + 0.05);
		canvasCtx.beginPath();
			canvasCtx.moveTo(this.x, this.y);
			canvasCtx.lineTo(this.x+(this.vx*8), this.y + (this.vy*8))
		canvasCtx.strokeStyle = 'rgb(255,255,255)';
		canvasCtx.stroke();
		if(this.x >= WIDTH || this.x <= 0 || this.y >= HEIGHT || this.y <= 0){
			this.active = false;
		}
	}
	function draw() {
		showFPS();
		//	Resize the canvas every frame to match the window size
		canvasCtx.canvas.width = WIDTH = window.innerWidth;
		canvasCtx.canvas.height = HEIGHT = window.innerHeight;
		//	Check if this is still the selected visualization style
		if(selected === 'Waveform'){
			requestAnimationFrame(draw);
		}
		ANALYSER.fftSize = 256;
		var bufferLength = ANALYSER.frequencyBinCount;
		var dataArray = new Uint8Array(bufferLength);
		//	Fills 'dataArray' with frequency data from the audio source.
		ANALYSER.getByteFrequencyData(dataArray);
		const grd = canvasCtx.createLinearGradient(0, 0, 170, canvasCtx.canvas.height);
		//	Color the background
		grd.addColorStop(0, 'rgba(0, 0, 0, 1.0)');
		grd.addColorStop(1, 'rgba(0, 0, 0, 1.0)');
		//	Apply the gradient to the next rectangle to be drawn, then set it as the background
		canvasCtx.fillStyle = grd;
		canvasCtx.fillRect(0, 0, canvasCtx.canvas.width, canvasCtx.canvas.height);
		for(let i=0; i< stars.length; i++){
			if(stars[i].active === true){
				stars[i].moveStar(i);
			}
			else{
				stars[i].createStar();
			}
		}
	}
	draw();
}
*/
</script>
<style>
  body, html{
    margin: 0;
    padding: 0;
    -webkit-user-select: none; /* Chrome/Safari */        
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* IE10+ */
    overflow-x: hidden;
  }
  canvas{
    position: absolute;
    background-color: transparent;
  }
  /*	
  Slider menu button	
  */
  #settings-button{
    position: absolute;
    top: 15;
    left: 15;
    background-color: #33b5e5;
    border-radius: 50%;
    padding: 12px 13px 12px 15px;
    transition: 0.4s;
    transform: translate(0px, 0px);
    z-index: 15;
  }
  #settings-button:hover{
    background-color: white;
    cursor: pointer;
  }

  /*
  Slide-out side menu
  */
  #side-menu{
    height: calc(100% - 25px);
    width: 510px;
    position: absolute;
    top: 0;
    left: 0;
    border-right-style: solid;
    border-right-width: 1px;
    border-right-color: rgba(15, 15, 15, 0.65);
    overflow-x: hidden;
    overflow-y: auto;
    transition: 0.4s;
    background-color: rgba(25, 25, 45, 0.65);
    transform: translate(-600px, 0px);
    z-index: 15;
    cursor: default;
    padding: 5px 0px 20px 0px;
  }

  #side-menu::-webkit-scrollbar-track{
    border-radius: 10px;
  }

  #side-menu::-webkit-scrollbar{
    border-radius: 10px;
    width: 1px;
  }
  #side-menu::-webkit-scrollbar-thumb{
    border-radius: 10px;
    background-color: rgba(0, 0, 0, 0.65);
  }

  .section-header{
    color: #33b5e5;
    padding: 10px 0px 10px 15px;
    font-family: "Muli", sans-serif;
    font-size: 25px;
    background-color: rgba(0, 0, 0, 0.65);
    margin: 15px 30px 0px 30px;
  }

  .settings-subsection{
    color: #33b5e5;
    padding: 10px 17px;
    margin: 0px 30px;
    font-family: Candara, Calibri, Segoe, "Segoe UI", Optinma, Arial, sans-serif;
    font-size: 21px;
  }
  .settings-subsection p{
    margin: 0;
    padding: 12px 0px 0px 1px;
    color: #DEDEDE;
    font-size: 17px;
  }

  /*
  Visualization Style Picker Stuff
  */
  .generic-menu-item{
    color: #DEDEDE;
    padding: 10px 0px 10px 17px;
    font-size: 18px;
    margin: 0px 30px;
    cursor: pointer;
    font-family: Candara, Calibri, Segoe, "Segoe UI", Optinma, Arial, sans-serif;
  }
  .generic-menu-item.selected{
    background-color: rgba(65, 65, 65, 0.65);
  }

  .generic-menu-item:hover{
    background-color: rgba(65, 65, 65, 0.65);
  }

  /*	Visualization Style Settings	*/
  .settings-item-container{
    margin: 0px 30px;
    padding: 10px 6px 10px 17px;
  }
  .slider-label{
    display: inline-block;
    font-family: Arial, sans-serif;
    color: #DEDEDE;
    font-size: 15px;
    width: 160px;
  }
  .slider-value{
    float: right;
  }
  .slider{
    display: inline-block;
    width: 240px;
    float: right;
    margin-top: 7px;
  }

  /*	Toggle switch	*/
  .switch{
    position: relative;
    display: inline-block;
    width: 50px;
    height: 23px;
    margin-right: 28px;
  }
  .switch input{
    display: none;
  }
  .toggle-switch{
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 2px;
    right: 0;
    bottom: 0;
    transition: .4s;
    border-radius: 34px;
    background-color: rgba(65, 65, 65, 0.65);
  }
  .toggle-switch:before{
    position: absolute;
    content: "";
    height: 19px;
    width: 19px;
    left: 4px;
    bottom: 2px;
    background-color: #dedede;
    transition: .4s;
    border-radius: 34px;
  }
  input:checked + .toggle-switch{
    background-color: #23a5d5;
  }
  input:checked + .toggle-switch:before {
    transform: translateX(22px);
  }
  .toggle-label{
    padding: 0px 10px 15px 0px;
    display: inline-block;
    vertical-align: middle;
    font-family: Arial, sans-serif;
    color: #DEDEDE;
    font-size: 15px;
  }
  #bars-settings{
    display: none;
  }
  .hide{
    display: none;
  }
</style>
```
