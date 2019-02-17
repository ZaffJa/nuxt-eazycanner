<template>
  <div
    v-if="toastText && toastType"
    :class="[toastType]"
    class="m-0 p-0 position-fixed text-white w-100 container-fluid text-center"
    style="top: 0px; z-index: 999; left: 0px"
  >
    <span>
      <strong>{{ toastText }}</strong>
    </span>
  </div>
</template>

<script>
export default {
  props: {
    toast: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {
      toastText: '',
      toastType: ''
    }
  },
  watch: {
    toast(newVal, oldVal) {
      this.toastText = newVal.text
      this.toastType = 'bg-' + newVal.type
      this.removeToast()
    }
  },
  methods: {
    removeToast() {
      setTimeout(() => {
        this.toastText = ''
        this.toastType = ''
      }, 4000)
    }
  }
}
</script>
