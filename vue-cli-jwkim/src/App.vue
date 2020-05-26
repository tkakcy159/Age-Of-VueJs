<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Hello-World msg="Welcome to Your Vue.js App"></Hello-World>
    <!-- 컴포넌트 네이밍 컨벤션들 -->
    <!-- 
      <hello-world></hello-world> => 이 방법이 권장된다고 함(VSCode에서 파일 바로가기 지원하는 네이밍 컨벤션)
      <HelloWorld></HelloWorld>
      <HelloWorld/>
    -->

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    'Hello-World': HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
