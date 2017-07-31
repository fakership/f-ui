<template>
  <div class="page-badge">
    <div class="page-title">Badge</div>

    <div class="page-badge-container">
      <div class="page-part">
        <f-badge type="primary" size="large">30</f-badge>
        <f-badge type="error" size="large">10</f-badge>
        <f-badge type="success" size="large">10</f-badge>
        <f-badge type="warning" size="large">10</f-badge>
      </div>

      <div class="page-part">
        <f-badge type="primary">30</f-badge>
        <f-badge type="error">10</f-badge>
        <f-badge type="success">10</f-badge>
        <f-badge type="warning">10</f-badge>
      </div>

      <div class="page-part">
        <f-badge type="primary" size="small">30</f-badge>
        <f-badge type="error" size="small">10</f-badge>
        <f-badge type="success" size="small">10</f-badge>
        <f-badge type="warning" size="small">10</f-badge>
      </div>

      <div class="page-part">
        <f-badge size="small" color="#888">自定义颜色</f-badge>
      </div>
    </div>

    <div class="page-part">
      <f-cell title="徽章">
        <span style="margin-right: 5px;">未读消息</span>
        <f-badge type="error" size="small">10</f-badge>
      </f-cell>
    </div>
  </div>
</template>

<script>
export default {
  name: 'page-badge'
};
</script>

<style lang="css">
  .page-badge-container {
    padding: 0 10px;
  }
</style>
