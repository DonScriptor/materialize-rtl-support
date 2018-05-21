# Materialize RTL
materialize rtl support (v1.0.0-rc.1)

CSS: 100% 💯
Components: 100% 💯
Javascript: 98% 🥇
 - Carousel: !!😓 carousel-item direction
 - Tabs: !!😓 indicator -> https://github.com/atechni/materialize-rtl-support/blob/master/dist/js/tabs.js

Forms: 99% 🥇
 - Range: !!😓 HTML5 thumb direction

1)_ [Download](https://github.com/atechni/materialize-rtl-support/archive/v1.0.0-rc.1.zip) and added after original materialize:
```html
<!-- materialize -->
<link rel="stylesheet" href="materialize.min.css"/>

<!-- materialize right-to-left -->
<link rel="stylesheet" href="materialize.rtl.min.css"/>
```

2)_ CDN:
```html
<!-- latest materialize -->
<link rel="stylesheet" href="https://rawgit.com/Dogfalo/materialize/1.0.0-rc.1/dist/css/materialize.min.css"/>

<!-- materialize right-to-left -->
<link rel="stylesheet" href="https://rawgit.com/mohamedlounnas/materialize-rtl/v1.0.0-rc.1/dist/css/materialize.rtl.min.css"/>
```

material icons (add the class "rtlx"):
[Which icons should be mirrored for RTL?](https://google.github.io/material-design-icons/#which-icons-should-be-mirrored-for-rtl-)
```html
<i class="material-icons rtlx">play_arrow</i>
```

Navbar:
```html
  <nav>
    <div class="nav-wrapper">
      <a href="#" class="brand-logo">Logo</a>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li><a href="sass.html">Sass</a></li>
        <li><a href="badges.html">Components</a></li>
        <li><a href="collapsible.html">JavaScript</a></li>
      </ul>
    </div>
  </nav>
```
  
Sidenav:
```javascript
$('.sidenav').sidenav({
  edge: 'right'
});
```

Range:  
```javascript
// -> https://refreshless.com/nouislider/slider-options/#section-direction
var slider = document.getElementById('my-range');
noUiSlider.create(slider, {
  //...
  direction: 'rtl',
  //...
});
```

Tabs:  
```javascript
// -> https://github.com/atechninfo/materialize-rtl/blob/master/js/tabs.js
$('ul.tabs').tabs({
   //...
   direction: 'auto', // default -> auto detect page direction rtl|ltr
   //...
});
```

functions:
```javascript
/**
 * detect page direction 
 */
function isRTL(el)
{
  var x = document.getElementById(el) || document.body; // if "el" empty -> get body direction
  if (x.currentStyle)
  var y = x.currentStyle['direction'];
   else if (window.getComputedStyle)
  var y = document.defaultView.getComputedStyle(x, null).getPropertyValue('direction');
  if (y == 'rtl') {
    return true;
  } else {
    return false;
  }
}
```

Enjoy ;)
