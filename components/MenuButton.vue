<template>
  <button :class="{'active': active}">
    <span class="line"></span>
  </button>
</template>

<script>
export default {
  props: {
    active: {
      type: Boolean,
      default: false
    }
  }
}
</script>


<style lang='scss' scoped>
button {
  width: 32px;
  height: 28px;
  background: transparent;
  border: none;
  position: relative;
  cursor: pointer;

  &::before,
  &::after {
    content: "";
    left: 0;
    position: absolute;
    height: 2px;
    width: 32px;
    transition: all 0.3s ease 0s;
    background: #414141;
    border-radius: 2px;
  }

  &::before {
    top: 0;
  }

  &::after {
    bottom: 0;
  }

}

.active {
  & .line {
    transform: scale(0) translate(0, -50%);
  }

  &::before {
    top: calc(50% - 2px);
    transform: rotate(45deg);
  }

  &::after {
    width: 32px;
    bottom: 50%;
    transform: rotate(135deg);
  }
}

.line {
  left: 0;
  position: absolute;
  height: 2px;
  width: 100%;
  transition: all 0.3s ease 0s;
  background: #414141;
  border-radius: 2px;
  top: 50%;
  transform: scale(1) translate(0, -50%);
}
</style>
