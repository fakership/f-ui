<template>
  <div class="page-cell">
    <div class="page-title">Cell</div>
    <f-cell title="标题文字"></f-cell>
    <f-cell title="标题文字" value="说明文字"></f-cell>
    <f-cell title="标题文字" icon="more" value="带 icon"></f-cell>
    <f-cell title="标题文字" icon="more">
      <span>icon 是图片</span>
      <img slot="icon" src="../assets/100x100.png" width="24" height="24">
    </f-cell>
    <f-cell title="标题文字" is-link value="带链接"></f-cell>
    <f-cell title="标题文字" is-link>
      <span style="color: green">这里是元素</span>
    </f-cell>
    <f-cell title="标题文字">
      <f-button size="small" type="primary" icon="back">按钮</f-button>
    </f-cell>

    <f-cell title="标题" label="描述信息" is-link></f-cell>

    <f-cell title="原生跳转" label="跳转到 https://f-ui.github.io" is-link to="https://f-ui.github.io"></f-cell>
    <f-cell title="路由跳转" label="跳转到 /#/toast" is-link :to="{ name: 'Toast' }"></f-cell>
  </div>
</template>
