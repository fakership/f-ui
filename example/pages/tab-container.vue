<template>
  <div>
    <div class="nav">
      <f-button size="small" @click.native.prevent="active = 'tab-container1'">tab 1</f-button>
      <f-button size="small" @click.native.prevent="active = 'tab-container2'">tab 2</f-button>
      <f-button size="small" @click.native.prevent="active = 'tab-container3'">tab 3</f-button>
    </div>
    <div class="page-tab-container">
      <f-tab-container class="page-tabbar-tab-container" v-model="active" swipeable>
        <f-tab-container-item id="tab-container1">
          <f-cell v-for="n in 10" title="tab-container 1"></f-cell>
        </f-tab-container-item>
        <f-tab-container-item id="tab-container2">
          <f-cell v-for="n in 5" title="tab-container 2"></f-cell>
        </f-tab-container-item>
        <f-tab-container-item id="tab-container3">
          <f-cell v-for="n in 7" title="tab-container 3"></f-cell>
        </f-tab-container-item>
      </f-tab-container>
    </div>
  </div>
</template>

<script>
export default {
  name: 'page-tab-container',
  data() {
    return {
      active: 'tab-container1'
    };
  }
};
</script>

<style lang="css" scoped>
  .item {
    display: inline-block;
  }

  .nav {
    padding: 10px;
  }

  .link {
    color: inherit;
    padding: 20px;
    display: block;
  }
</style>
