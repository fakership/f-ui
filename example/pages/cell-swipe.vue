<template>
  <div class="page-cell">
    <div class="page-title">Cell Swipe</div>
    <f-cell-swipe
      v-for="n in 10"
      :right="rightButtons"
      title="swipe me">
    </f-cell-swipe>
  </div>
</template>

<script>
  export default {
    created() {
      this.rightButtons = [
        {
          content: 'Mark as Unread',
          style: { background: 'lightgray', color: '#fff' }
        },
        {
          content: 'Delete',
          style: { background: 'red', color: '#fff' },
          handler: () => this.$messagebox('delete')
        }
      ];
    },

    methods: {
      leftButtonHandler(evt) {
        console.log(123);
      }
    }
  };
</script>
