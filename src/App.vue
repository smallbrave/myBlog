<template>
  <div id="app">
    <MyButton type="primary" disabled @click="confirm">提交</MyButton>
    <MyInput type="text" v-model="value" disabled @input="handleInput"></MyInput>
  </div>
</template>

<script>
import MyButton from '@/myComponents/MyButton.vue';
import MyInput from '@/myComponents/MyInput.vue';

export default {
  name: 'App',
  components: {
    MyButton,
    MyInput,
  },
  data() {
    return {
      value: '',
    };
  },
  methods: {
    confirm() {
      console.log('提交');
    },
    handleInput(val) {
      console.log(val);
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
