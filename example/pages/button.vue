<template>
  <div class="page-button">
    <h1 class="page-title">Button</h1>
    <div class="page-button-group">
      <f-button size="large">default</f-button>
      <f-button size="large" type="primary">primary</f-button>
      <f-button size="large" type="danger">danger</f-button>
    </div>

    <div class="page-button-group">
      <f-button>default</f-button>
      <f-button type="primary">primary</f-button>
      <f-button type="danger">danger</f-button>
    </div>

    <div class="page-button-group">
      <f-button size="small">default</f-button>
      <f-button size="small" type="primary">primary</f-button>
      <f-button size="small" type="danger">danger</f-button>
    </div>

    <div class="page-button-group">
      <f-button disabled size="large">default</f-button>
      <f-button disabled size="large" type="primary">primary</f-button>
      <f-button disabled size="large" type="danger">danger</f-button>
    </div>

    <div class="page-button-group">
      <f-button plain size="large">default</f-button>
      <f-button plain size="large" type="primary">primary</f-button>
      <f-button plain size="large" type="danger">danger</f-button>
    </div>

    <div class="page-button-group">
      <f-button>
        <img src="../assets/100x100.png" height="20" width="20" slot="icon">
        带自定义图标
      </f-button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'button'
};
</script>

<style lang="css">
  @component-namespace page {
    @component button {
      padding: 0 15px 15px;

      @descendent group {
        margin-bottom: 15px;

        & > * {
          margin-bottom: 15px;
        }
      }
    }
  }
</style>
