<template>
  <div id="app">
    <Button type="primary" disabled @click="confirm">
      提交
    </Button>
  </div>
</template>

<script>
import Button from '@/myComponents/Button.vue';

export default {
  name: 'App',
  components: {
    Button,
  },
  methods: {
    confirm() {
      console.log('提交');
    },
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
