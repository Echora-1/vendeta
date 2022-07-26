<template>
  <div :class="{'input-focused': focused, 'show-label': valueNotEmpty, 'invalid': requiredStatus && touched || invalid}">
    <label :for="id" class="base-label">
      {{ label }}
    </label>
    <div
      class='base-input-wrapper'
    >
      <input
        :id="id"
        class="base-input"
        v-bind="$attrs"
        :value="value"
        @focus="focusHandler"
        @input="inputHandler"
        @blur="blurHandler"
      >
      <p v-show='requiredStatus && touched || invalid' class='invalid-text'>Required field</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: ''
    },

    id: {
      type: String,
      default: ''
    },
    label: {
      type: String,
      default: ''
    },
    invalid: {
      type: Boolean,
      default: false
    },

    requiredField: {
      type: Boolean,
      default: false
    },
  },

  data() {
    return {
      focused: false,
      touched: false
    }
  },

  computed: {
    valueNotEmpty() {
      return this.value.length > 0
    },
    requiredStatus(){
      if(this.requiredField) {
        return  this.value.length === 0
      }
      return false
    }
  },

  methods: {
    inputHandler(event) {
      // eslint-disable-next-line vue/no-mutating-props
      this.$emit('input', event.target.value)
    },

    focusHandler() {
      this.focused = true
    },

    blurHandler() {
      this.touched = true
      this.focused = false
    }
  }
}
</script>

<style lang='scss' scoped>

.base-input-wrapper {
  border: 2px solid rgba(87, 98, 128, 0.4);
  width: 100%;
  transition: all 0.5s;
  position: relative;
  border-radius: 40px;
  margin-bottom: 25px;
}

.base-input {
  width: 100%;
  margin: 0;
  border: none;
  outline: none;
  padding: 13px 24px;
  background: transparent;
  font-size: 18px;
  line-height: 26px;
  color: #161616;
}

.base-input::placeholder ,{
  color: rgba(87, 98, 128, 0.4);
}

label {
  display: none;
}

.input-focused {
  .base-input-wrapper {
    border-color: #00B4DB;
  }
}

.invalid {
  .base-input-wrapper {
    border-color: #DB0D00;
  }
}

.invalid-text {
  color: #DB0D00;
  position: absolute;
  bottom: -35px;
  left: 25px;
  font-size: 13px;
  line-height: 19px;
}

</style>
