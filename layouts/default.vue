<template>
  <div class="default-layouts">
    <base-header />
    <main>
      <Nuxt />
    </main>
  </div>
</template>
<script>
import BaseHeader from '~/components/base/BaseHeader'
export default {
  components: { BaseHeader },
}
</script>

<style lang="scss" scoped>
.default-layouts {
  overflow: hidden;
}
</style>
