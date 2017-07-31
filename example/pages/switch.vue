<template>
  <div class="page-switch">
    <div class="page-title">Switch</div>
    <div class="page-part page-switch-padding">
      <f-switch v-model="value1" @change="handleChange">
        <label v-text="value1"></label>
      </f-switch>
    </div>

    <div class="page-part page-switch-padding">
      <f-switch v-model="value4" @change="handleChange">
        <label v-text="value4"></label>
      </f-switch>
    </div>

    <f-cell :title="'选项 ' + value2">
      <f-switch v-model="value2" @change="handleChange"></f-switch>
    </f-cell>
    <f-cell :title="'选项 ' + value3">
      <f-switch v-model="value3" @change="handleChange"></f-switch>
    </f-cell>
  </div>
</template>

<script>
export default {
  name: 'page-switch',

  data() {
    return {
      value1: false,
      value2: false,
      value3: true,
      value4: true
    };
  },

  methods: {
    handleChange(event) {
      console.log(event);
    }
  }
};
</script>

<style lang="css">
  @component-namespace page {
    @component switch {
      @descendent padding {
        padding: 0 10px;
      }
    }
  }
</style>
