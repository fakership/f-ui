<template>
  <div class="f-progress">
    <slot name="start"></slot>
    <div class="f-progress-content">
      <div class="f-progress-runway" :style="{ height: barHeight + 'px' }"></div>
      <div class="f-progress-progress" :style="{ width: value + '%', height: barHeight + 'px' }"></div>
    </div>
    <slot name="end"></slot>
  </div>
</template>

<style>
  @component-namespace f {
    @component progress {
      position: relative;
      display: flex;
      height: 30px;
      line-height: 30px;

      & > * {
        display: flex;
        display: -webkit-box;
      }

      & *[slot="start"] {
        margin-right: 5px;
      }

      & *[slot="end"] {
        margin-left: 5px;
      }

      @descendent content {
        position: relative;
        flex: 1;
      }

      @descendent runway {
        position: absolute;
        transform: translate(0, -50%);
        top: 50%;
        left: 0;
        right: 0;
        background-color: #ebebeb;
        height: 3px;
      }

      @descendent progress {
        position: absolute;
        display: block;
        background-color: #26a2ff;
        top: 50%;
        transform: translate(0, -50%);
        width: 0;
      }
    }
  }
</style>

<script type="text/ecmascript-6">
  export default {
    name: 'f-progress',

    props: {
      value: Number,
      barHeight: {
        type: Number,
        default: 3
      }
    }
  };
</script>
