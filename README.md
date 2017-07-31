# F-UI

## 开头
`f-ui`此项目是基于`elemefe`的`mint-ui`来搭建的项目，后续本人会持续的维护改进.

## 可能会出现的问题
`f-ui`尽可能使用`yarn`进行安装，`npm`下会出现一些问题。

## 技术体系

`f-ui`是基于`vue2.0`。

	* js方面采用`es6`格式书写
	* css模块化用的是`postcss`
	* 代码规范上采用`eleme`的配置`eslint-config-eleme`
	* 打包方面采用基于`webpack`的`cooking`
	* 采用`lerna`作为多npm包的发布方式
	* 通过`sh`实现了一键化打包、部署、推送

## 如何添加组件？

1. 在项目根目录下的`packages`里添加你想添加组件的目录，如果不需要支持`js`的方式进行调用，则只需要添加`[name].vue`文件即可，如果需要支持`js`，则还需要添加`[name].js`。
2. 在根目录下的`components.json`里写入这个组件

## make命令的使用

* make dev: 启动开发环境,会开启`example`的相关网站，对`example`进行开发
* make pub: 发布`f-ui`的版本
* make pub-all: 发布所有的组件版本
* 更多命令请看`makefile`文件

## Usage

导入全部组件的方式

```javascript
import Vue from 'vue';
import F from 'f-ui';
import 'f-ui/lib/style.css';

Vue.use(F);
```
按需导入组件
[babel-plugin-component](https://www.npmjs.com/package/babel-plugin-component)

```javascript
import { Cell, Checklist } from 'f-ui';

Vue.component(Cell.name, Cell);
Vue.component(Checklist.name, Checklist);
```
相当于

```javascript
import Vue from 'vue';
import F from 'f-ui';
import 'f-ui/lib/style.css';

Vue.use(F);

// import specified component

import FRadio from 'f-ui/lib/radio';
import 'f-ui/lib/radio/style.css';

Vue.component(FRadio.name, MtRadio);
```

## babel-plugin-component
- Auto import css file
- Modular import component

Installation
```shell
npm i babel-plugin-component -D
```

如何使用这个插件?

更改项目下的`.babelrc`文件

```json
{
  "plugins": ["other-plugin", ["component", [
    { "libraryName": "f-ui", "style": true }
  ]]]
}
```
