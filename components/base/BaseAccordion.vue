<template>
    <div class="tab">
      <input :id="content.title" type="checkbox">
      <label class="tab-label" :for="content.title">{{ content.title }}<icon-arrow /></label>
      <div class="tab-content">
        <p v-for='(item, index) in content.text' :key='index'>{{ item }}</p>
      </div>
    </div>
</template>

<script>
import IconArrow from "@/components/icon/IconArrow";
export default {
  components: {IconArrow},
  props: {
    content: {
      type: Object,
      default: () => {
        return {
          title: '',
          text: []
        }
      }
    },
  }
}
</script>

<style lang='scss' scoped>
input {
  position: absolute;
  opacity: 0;
  z-index: -1;
}

input:checked {
  + .tab-label {
    color: #00B4DB;
    svg {
      transform: translateY(-50%) rotate(180deg);
    }
  }
  ~ .tab-content {
    max-height: 100vh;
    padding: 20px 34px;
  }
}

.tab {
  background: #FFFFFF;
  border-radius: 12px;
  width: 100%;
  color: #414141;
  overflow: hidden;
  &-label {
    display: flex;
    justify-content: space-between;
    padding: 24px 50px 24px 34px;
    background: #FFFFFF;
    color: #414141;
    cursor: pointer;
    font-size: 18px;
    line-height: 24px;
    position: relative;
    transition: color 0.3s;

    @media(max-width: 767px) {
      font-size: 16px;
    }

    svg {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      right: 30px;
      transition: all 0.3s;
    }
  }
  &-content {
    max-height: 0;
    padding: 0 34px;
    font-size: 16px;
    line-height: 24px;
    color: #33333399;
    background: #FFFFFF;
    transition: all .35s;
    position: relative;

    p {
      margin: 0;
    }

    p:not(:last-child) {
      margin-bottom: 30px;
    }

    &::before {
      content: "";
      position: absolute;
      background: rgba(10, 10, 10, 0.1);
      height: 1px;
      left: 50%;
      transform: translateX(-50%);
      top: 0;
      width: calc(100% - 60px);
    }
  }
}

</style>
