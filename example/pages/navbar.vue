<template>
  <div class="page-navbar">
    <div class="page-title">Navbar</div>
    <f-navbar class="page-part" v-model="selected">
      <f-tab-item id="1">选项一</f-tab-item>
      <f-tab-item id="2">选项二</f-tab-item>
      <f-tab-item id="3">选项三</f-tab-item>
    </f-navbar>

    <div>
      <f-cell class="page-part" title="当前选中">{{ selected }}</f-cell>
    </div>

    <f-tab-container v-model="selected">
      <f-tab-container-item id="1">
        <f-cell v-for="n in 10" :title="'内容 ' + n" />
      </f-tab-container-item>
      <f-tab-container-item id="2">
        <f-cell v-for="n in 4" :title="'测试 ' + n" />
      </f-tab-container-item>
      <f-tab-container-item id="3">
        <f-cell v-for="n in 6" :title="'选项 ' + n" />
      </f-tab-container-item>
    </f-tab-container>
  </div>
</template>

<script>
export default {
  name: 'page-navbar',

  data() {
    return {
      selected: '1'
    };
  }
};
</script>
