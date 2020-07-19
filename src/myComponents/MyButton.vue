<template>
  <div class="btn-wrapper">
    <button
      :class="type+ ' ' + size"
      :type="type"
      :disabled="disabled"
      @click="handleClick"
    >
      <slot>确认</slot>
    </button>
  </div>
</template>
<script>
export default {
  props: {
    type: {
      type: String,
      default: 'default',
    },
    size: {
      type: String,
      default: 'default',
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    handleClick(event) {
      this.$emit('click', event);
    },
  },
};
</script>
<style>
button {
    display: inline-block;
    padding: 0;
    box-sizing: border-box;
    border: 1px solid transparent;
    border-radius: 5px;
}

button:hover {
  cursor: pointer;
}

.default {
    width: 80px;
    height: 40px;
    line-height: 40px;
    font-size: 20px;
    color: #000;
    background-color: #fcefef;
}

.primary {
    color: #fff;
    background-color: #337ab7;
}

.danger {
    color: #fff;
    background-color: #d9534f;
}

.info {
    color: #fff;
    background-color: #5bc0de;
}

.success {
    color: #fff;
    background-color: #5cb85c;
}

.warning {
    color: #fff;
    background-color: #f0ad4e;
}

.small {
    width: 40px;
    height: 20px;
    line-height: 20px;
    font-size: 12px;
}

.large {
    width: 120px;
    height: 60px;
    line-height: 60px;
    font-size: 28px;
}
/* 使用属性选择器 */
button[disabled] {
  cursor: not-allowed;
  opacity: .5;
}
</style>
