<template>
  <div v-show="title === selectedTitle" class="tab-content">
    <slot />
  </div>
</template>

<script >
export default  {
  inject: ['selectedTitle'],
  props: {
    title: {
      type: String,
      default: ""
    }
  }
}
</script>
