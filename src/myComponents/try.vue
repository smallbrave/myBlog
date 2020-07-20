<template>
  <div class="try-container">
    测试一下 {{ msg }}
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: '这是一个小小的消息',
    };
  },
};
</script>
<style>
.try-container {
  background-color: #ccc;
}
</style>
