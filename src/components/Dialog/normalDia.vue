<template>
  <div class="modal modal-in">
    <div class="modal-inner">
      <div>{{ msg.tit }}</div>
      <div>{{ msg.content }}</div>
    </div>
    <div class="modal-btns">
      <span class="modal-btn modal-button-bold" @click="cancel">确定</span>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      msg: {
        type: Object,
        required: true,
        default: {}
      }
    },
    methods: {
      cancel () {
        this.$dispatch('cancel')
      }
    }
  }
</script>
