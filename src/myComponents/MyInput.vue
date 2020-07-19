<template>
  <div class='input-container'>
    <input :type='type' :value='value' @input='handleInput' />
  </div>
</template>
<script>
export default {
  props: {
    type: {
      type: String,
      default: 'text',
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    value: {
      type: String,
      default: '',
    },
  },
  methods: {
    handleInput(event) {
      this.$emit('input', event.target.value);
      // 此处不是简单的使用this.value；而是使用event事件源 => 通过event.target.value获取值
    },
  },
};
</script>
<style>
input {
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: transparent;
  font-family: inherit;
  cursor: pointer;
  background-color: #fff;
  background-image: none;
  border-radius: 4px;
  border: 1px solid #dcdfe6;
  box-sizing: border-box;
  color: #606266;
  display: inline-block;
  font-size: inherit;
  height: 40px;
  line-height: 40px;
  outline: none;
  padding: 0 15px;
  transition: border-color 0.2s cubic-bezier(0.645, 0.045, 0.355, 1);
  width: 100%;
}

input[disabled] {
  cursor: not-allowed;
}
</style>
