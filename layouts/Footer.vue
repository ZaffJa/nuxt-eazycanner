<template>
  <div class="bg-main p-3 mt-5 text-white blockquote-footer text-right">
    Copyright © {{ now }} Eazy Canner Sdn Bhd
  </div>
</template>

<script>
export default {
  data() {
    return {
      now: new Date().getFullYear()
    }
  }
}
</script>
