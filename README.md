# F UI

## 开头
`f-ui`此项目是基于`elemefe`的`mint-ui`来搭建的项目，后续本人会持续的维护改进.

## 技术体系
`f-ui`是基于`vue2.0`。
* js方面采用`es6`格式书写
* css模块化用的是`postcss`
* 代码规范上采用`eleme`的配置`eslint-config-eleme`
* 打包方面采用基于`webpack`的`cooking`
* 采用`lerna`作为多npm包的发布方式
* 通过`sh`实现了一键化打包、部署、推送

## 如何添加组件？
在项目根目录下的`packages`里添加你想添加组件的目录，如果不需要支持`js`的方式进行调用，则只需要添加`[name].vue`文件即可，如果需要支持`js`，则还需要添加`[name].js`。

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
