<template>
  <div v-if="dialog" class="bg__gray">
    <div class="dialog__box" slot="info">
      <span>{{ title }}</span>
      <span class="close" @click="closeDialog">&times;</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title'
    },
    open: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({
    // 由父層控制 或是 本身狀態控制
    dialog: false
  }),
  methods: {
    toggle(value) {
      this.dialog = value;
    },
    closeDialog() {
      this.dialog = false
    },
    init(){
      console.log('dialog init')
    }
  },
  computed: {},
  mounted() {
    this.init()
  }
}
</script>

<style>
/**
phone
 */
@media (max-width: 576px) {


  .bg__gray {
    background-color: rgb(0, 0, 0); /* Fallback color */
    background-color: rgba(0, 0, 0, 0.4); /* Black w/ opacity */
    z-index: 999;
    height: 100%;
    width: 100%;
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .dialog__box {
    background-color: white;
    border-radius: 10px;
    height: 500px;
    width: 300px;
    overflow: auto;
  }

  .close {
    color: #aaaaaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }

  .close:hover, .close:focus {
    color: #000;
    text-decoration: none;
    cursor: pointer;
  }
}

</style>
