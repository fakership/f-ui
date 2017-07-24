# F UI

## Installation
```shell
npm i f-ui -S
```

## Usage

Import all components.

```javascript
import Vue from 'vue';
import F from 'f-ui';
import 'f-ui/lib/style.css';

Vue.use(F);
```

Or import specified component. (Use [babel-plugin-component](https://www.npmjs.com/package/babel-plugin-component))

```javascript
import { Cell, Checklist } from 'f-ui';

Vue.component(Cell.name, Cell);
Vue.component(Checklist.name, Checklist);
```


Equals to

```javascript
import Vue from 'vue';
import Mint from 'f-ui';
import 'f-ui/lib/style.css';

Vue.use(Mint);

// import specified component

import MtRadio from 'f-ui/lib/radio';
import 'f-ui/lib/radio/style.css';

Vue.component(MtRadio.name, MtRadio);
```

## babel-plugin-component
- Auto import css file
- Modular import component

Installation
```shell
npm i babel-plugin-component -D
```

Usage

.babelrc
```json
{
  "plugins": ["other-plugin", ["component", [
    { "libraryName": "f-ui", "style": true }
  ]]]
}
```

## Development

```shell
npm run dev
```

## License
MIT
