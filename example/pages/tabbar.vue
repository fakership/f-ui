<template>
  <div class="page-tabbar">
    <div class="page-wrap">
      <div class="page-title">Tabbar</div>
      <div>
        <f-cell class="page-part" title="当前选中" :value="selected" />
      </div>

      <f-tab-container class="page-tabbar-container" v-model="selected">
        <f-tab-container-item id="外卖">
          <f-cell v-for="n in 10" :title="'餐厅 ' + n" />
        </f-tab-container-item>
        <f-tab-container-item id="订单">
          <f-cell v-for="n in 5" :title="'订单 ' + n" />
        </f-tab-container-item>
        <f-tab-container-item id="发现">
          <f-cell v-for="n in 7" :title="'发现 ' + n" />
        </f-tab-container-item>
        <f-tab-container-item id="我的">
          <div class="page-part">
            <f-cell v-for="n in 12" :title="'我的 ' + n" />
          </div>
          <router-link to="/">
            <f-button type="danger" size="large">退出</f-button>
          </router-link>
        </f-tab-container-item>
      </f-tab-container>
    </div>

    <f-tabbar v-model="selected" fixed>
      <f-tab-item id="外卖">
        <img slot="icon" src="../assets/100x100.png">
        外卖
      </f-tab-item>
      <f-tab-item id="订单">
        <img slot="icon" src="../assets/100x100.png">
        订单
      </f-tab-item>
      <f-tab-item id="发现">
        <img slot="icon" src="../assets/100x100.png">
        发现
      </f-tab-item>
      <f-tab-item id="我的">
        <img slot="icon" src="../assets/100x100.png">
        我的
      </f-tab-item>
    </f-tabbar>
  </div>
</template>

<script>
export default {
  name: 'page-tabbar',
  data() {
    return {
      selected: '外卖'
    };
  }
};
</script>

<style>
  .page-tabbar {
    overflow: hidden;
    height: 100vh;
  }

  .page-wrap {
    overflow: auto;
    height: 100%;
    padding-bottom: 100px;
  }
</style>
