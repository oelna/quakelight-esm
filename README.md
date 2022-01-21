# Quakelight ESM

A small Javascript module to reproduce the original quake light flicker effect on websites

See also: https://www.alanzucconi.com/2021/06/15/valve-flickering-lights/

### Usage

```html
<div class="quakelight" data-preset="10" ></div>
<div class="quakelight" data-lightstring="mmmaaamabcdezzzaaa" ></div>
```

```javascript
import { quakelight } from './lights.js'

// elements with class .quakelight will be processed automatically
const ql = new quakelight();

// add manually with preset (0-11)
ql.add(document.querySelector('.customele'), 3);

// add manually with string (a=0.0, z=1.0)
ql.add(document.querySelector('.customele'), 'aaaaaammmmzzzzzmmmmm');

// remove from a specific node
ql.remove(document.querySelector('.customele'));

// remove all QL effects
ql.removeAll();

```

### Demo
https://oelna.github.io/quakelight-esm/ (stops after 5 seconds)
