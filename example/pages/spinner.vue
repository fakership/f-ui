<template>
  <div class="page-spinner">
    <div class="page-title">Spinner</div>

    <f-cell title="snake">
      <f-spinner color="#26a2ff" type="snake"></f-spinner>
    </f-cell>

    <f-cell title="double-bounce">
      <f-spinner color="#26a2ff" type="double-bounce"></f-spinner>
    </f-cell>

    <f-cell title="triple-bounce">
      <f-spinner color="#26a2ff" type="triple-bounce"></f-spinner>
    </f-cell>

    <f-cell title="fading-circle">
      <f-spinner color="#26a2ff" type="fading-circle"></f-spinner>
    </f-cell>
  </div>
</template>

<script>
export default {
  name: 'page-spinner',

  data() {
    return {

    };
  }
};
</script>

<style lang="css">
  @component-namespace page {
    @component spinner {
      .f-cell {
        min-height: 50px;
      }
    }
  }
</style>