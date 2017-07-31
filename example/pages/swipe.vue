<template>
  <div class="page-swipe">
    <h1 class="page-title">Swipe</h1>
    <p class="page-swipe-desc">基础用法</p>
    <f-swipe :auto="4000">
      <f-swipe-item class="slide1">1</f-swipe-item>
      <f-swipe-item class="slide2">2</f-swipe-item>
      <f-swipe-item class="slide3">3</f-swipe-item>
    </f-swipe>

    <p class="page-swipe-desc">隐藏 indicators</p>
    <f-swipe :show-indicators="false">
      <f-swipe-item class="slide1">1</f-swipe-item>
      <f-swipe-item class="slide2">2</f-swipe-item>
      <f-swipe-item class="slide3">3</f-swipe-item>
    </f-swipe>

    <p class="page-swipe-desc">取消自动播放</p>
    <f-swipe :auto="0">
      <f-swipe-item class="slide1">1</f-swipe-item>
      <f-swipe-item class="slide2">2</f-swipe-item>
      <f-swipe-item class="slide3">3</f-swipe-item>
    </f-swipe>

    <p class="page-swipe-desc">设置默认显示页</p>
    <f-swipe :auto="0" :defaultIndex="1">
      <f-swipe-item class="slide1">1</f-swipe-item>
      <f-swipe-item class="slide2">2</f-swipe-item>
      <f-swipe-item class="slide3">3</f-swipe-item>
    </f-swipe>

    <p class="page-swipe-desc">单个幻灯片</p>
    <f-swipe :show-indicators="false">
      <f-swipe-item class="slide1">SINGLE SLIDE</f-swipe-item>
    </f-swipe>
  </div>
</template>

<style>
  @component-namespace page {
    @component swipe {
      @descendent desc {
        text-align: center;
        color: #666;
        margin-bottom: 5px;
      }
      .f-swipe {
        height: 200px;
        color: #fff;
        font-size: 30px;
        text-align: center;
        margin-bottom: 20px;
      }

      .f-swipe-item {
        line-height: 200px;
      }

      .slide1 {
        background-color: #0089dc;
        color: #fff;
      }

      .slide2 {
        background-color: #ffd705;
        color: #000;
      }

      .slide3 {
        background-color: #ff2d4b;
        color: #fff;
      }
    }
  }
</style>
