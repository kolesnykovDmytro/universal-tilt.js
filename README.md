# universal-tilt.js

JavaScript & jQuery elements movement plugin based on:

**[Tilt.js](https://gijsroge.github.io/tilt.js/)** by **[Gijs Rogé](https://twitter.com/GijsRoge)** and **[vanilla-tilt.js](https://micku7zu.github.io/vanilla-tilt.js/index.html)** by **[Șandor Sergiu](https://github.com/micku7zu)**

**universal-tilt.js** contains additional functions for **mobile devices (having a gyroscope)** and new **Position Base option**

## Usage
At the beginning connect the library with Your project

**With script tag in HTML:**
```
<script src="/directory/to/library/folder/universal-tilt.js"></script>
```

**Include via command line and CommonJS/ES6 import:**
```
npm install universal-tilt.js // npm
yarn add universal-tilt.js // yarn
```

```
const UniversalTilt = require('universal-tilt.js'); // CommonJS
import UniversalTilt form 'universal-tilt.js'; // ES6
```
<br>

**Next use library with Vanilla JavaScript e.g:**
```
const tilts = document.querySelectorAll('.tilt');
const liveTilt = new UniversalTilt(tilts, {
   // options...
});
```

**or jQuery:**

*Connect jQuery in HTML*
```
<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
```

*or include via command line and CommonJS*
```
npm install jquery // npm
yarn add jquery // yarn
bower install jquery //bower
```

```
const jQuery = require('jquery');
```

*and call plugin on element*
```
$('.tilt').universalTilt({
   // options...
});
```

## Options
Name | Type | Default | Description | Available options
-|-|-|-|-
**position-base**| string | `element` | The surface from which the location of the mouse is captured | `element` or `window`
**reset** | boolean | `true` | Allow/disable element position reset after mouseout | `true` *(allow)*, `false` *(disable)*
**shadow** | boolean | `false` | Show/hide shadow effect | `true` *(allow)*, `false` *(disable)*
**shadow-save**<sup>1</sup> | boolean | `false` | Show/hide shadow effect | `true` *(allow)*, `false` *(disable)*
**shadow-color**<sup>1</sup> | string | `rgba(0, 0, 0, 0.4)` | Color of tilt element shadow | Color value in hex/rgb(a)/hsl/etc.
**shine** | boolean | `false` | Add/remove shine effect on mouseover | `true` *(add)*, `false` *(remove)*
**shine-opacity**<sup>2</sup> | number | `0` | Add/remove shine effect on mouseover | values >= 0  and <= 1
**shine-save**<sup>2</sup> | boolean | `false` | Save/reset shine effect on mouseout | `true` *(save)*, `false` *(reset)*
**max** | number | `35` | Max tilt value | e.g: `28`
**perspective** | number | `1000` | Tilt effect perspective | e.g: `700`
**scale** | number | `1.0` | Element scale on mouseover | `0.9`/`1.3`/etc.
**disabled** | string | `null` | Disable axis | `x` or `y`
**reverse** | boolean | `false` | Reverse tilt effect directory | `true` *(reverse directory)*, `false` *(standard directory)*
**speed** | string | `300ms` | Transition speed | `300ms`/`0.5s`/etc.
**easing** | string | `cubic-bezier(.03,.98,.52,.99)` | Transition easing | `cubic-bezier`/`ease`/`linear`/etc.

<sup>1</sup> *shadow value must be true*

<sup>2</sup> *shine value must be true*


## License
This project is licensed under the MIT License
