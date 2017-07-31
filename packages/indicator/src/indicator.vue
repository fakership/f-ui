<template>
  <transition name="f-indicator">
    <div class="f-indicator" v-show="visible">
      <div class="f-indicator-wrapper" :style="{ 'padding': text ? '20px' : '15px' }">
        <spinner class="f-indicator-spin" :type="convertedSpinnerType" :size="32"></spinner>
        <span class="f-indicator-text" v-show="text">{{ text }}</span>
      </div>
      <div class="f-indicator-mask" @touchmove.stop.prevent></div>
    </div>
  </transition>
</template>

<style>
@component-namespace f {
  @component indicator {
    transition: opacity .2s linear;

    @descendent wrapper {
      position: fixed 50% * * 50%;
      transform: translate(-50%, -50%);
      border-radius: 5px;
      background: rgba(0, 0, 0, 0.7);
      color: white;
      box-sizing: border-box;
      text-align: center;
    }

    @descendent text {
      display: block;
      color: #fff;
      text-align: center;
      margin-top: 10px;
      font-size: 16px;
    }

    @descendent spin {
      display: inline-block;
      text-align: center;
    }

    @descendent mask {
      position: fixed 0 * * 0;
      size: 100%;
      opacity: 0;
      background: transparent;
    }
  }
}

.f-indicator-enter,
.f-indicator-leave-active {
  opacity: 0;
}
</style>

<script type="text/babel">
  import Spinner from 'f-ui/packages/spinner/index.js';
  if (process.env.NODE_ENV === 'component') {
    require('f-ui/packages/spinner/style.css');
  }

  export default {
    data() {
      return {
        visible: false
      };
    },

    components: {
      Spinner
    },

    computed: {
      convertedSpinnerType() {
        switch (this.spinnerType) {
          case 'double-bounce':
            return 1;
          case 'triple-bounce':
            return 2;
          case 'fading-circle':
            return 3;
          default:
            return 0;
        }
      }
    },

    props: {
      text: String,
      spinnerType: {
        type: String,
        default: 'snake'
      }
    }
  };
</script>
