<template>
  <div class="page-progress">
    <h1 class="page-title">Progress</h1>
    <f-cell title="默认">
      <f-progress></f-progress>
    </f-cell>
    <f-cell title="设置 value">
      <f-progress :value="20"></f-progress>
    </f-cell>
    <f-cell title="左右文字">
      <f-progress :value="40">
        <div slot="start">0%</div>
        <div slot="end">100%</div>
      </f-progress>
    </f-cell>
    <f-cell title="定义线宽">
      <f-progress :value="60" :bar-height="5"></f-progress>
    </f-cell>
    <div class="page-progress-wrapper">
      <f-button size="large" type="primary" @click.native="uploadFile">上传文件</f-button>
      <f-progress :value="value" v-if="progressVisible" transition="progress-fade">
        <div slot="end">{{ value }}%</div>
      </f-progress>
    </div>
  </div>
</template>

<style>
  @component-namespace page {
    @component progress {
      .f-cell-value {
        flex: 2.5;
        position: relative;
        top: -20px;
      }

      .f-progress {
        width: 100%;
        position: absolute;
        top: 5px;
      }

      @descendent wrapper {
        padding: 0 10px;
        margin-top: 50px;

        .f-progress {
          position: relative;
        }

        .progress-fade-transition {
          transition: opacity .3s;
        }

        .progress-fade-enter,
        .progress-fade-leave {
          opacity: 0;
        }
      }
    }
  }
</style>

<script type="text/babel">
  import { Toast } from 'src/index';

  export default {
    data() {
      return {
        progressVisible: false,
        value: 0,
        uploading: false,
        timer: null
      };
    },

    watch: {
      value(val) {
        if (val >= 100) {
          this.uploading = false;
          this.progressVisible = false;
          setTimeout(() => Toast({ message: '上传成功', position: 'bottom', duration: 1000 }), 200);
          clearTimeout(this.timer);
        }
      }
    },

    methods: {
      uploadFile() {
        if (!this.uploading) {
          this.value = 0;
          this.progressVisible = true;
          this.uploading = true;
          this.timer = setInterval(() => this.value++, 10);
        }
      }
    }
  };
</script>