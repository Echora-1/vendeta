<template>
  <svg
    :width="width"
    :height="height"
    viewBox="0 0 20 21"
    fill="currentColor"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M0 2.84042L8.17337 1.72729L8.17694 9.61117L0.00746635 9.65769L0 2.84042ZM8.16947 10.5195L8.17582 18.4103L0.00634411 17.2871L0.00588605 10.4666L8.16947 10.5195ZM9.16028 1.58168L19.9975 0V9.5109L9.16028 9.59693V1.58168ZM20 10.5937L19.9975 20.0618L9.16025 18.5323L9.14507 10.576L20 10.5937Z"
      fill="currentColor"
    />
  </svg>
</template>

<script>
export default {
  props: {
    width: {
      type: String,
      default: "100%"
    },
    height: {
      type: String,
      default: "100%"
    },
  }
}
</script>
