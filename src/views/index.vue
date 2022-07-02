<template>
  <div>
    <img
      alt="Vue logo"
      src="../assets/logo.png"
    >
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <button @click="toTest">to test</button>
    <div class="c-red">{{state.count}}</div>
    <button @click="addCount">add count</button>

    <div>hello </div>
  </div>
</template>

<script setup>
import HelloWorld from '../components/HelloWorld.vue'
import { reactive } from 'vue';
import { useRouter }  from 'vue-router';

const router = useRouter()

const state = reactive({ count: 0 })

function toTest() {
  console.log(1);
  router.push('./test')
}

function addCount() {
  state.count++
}
</script>

<style lang="less" scoped>
.c-red{
  color: red;
}
</style>>


