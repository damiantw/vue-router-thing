<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>{{ $route.query.foo }}</div>
    <router-view></router-view>
    <router-link :to="{ name: 'page1', query: {foo: 'BLAH BLAH BLAH'}}" exact>Page1</router-link>
    <router-link :to="{ name: 'page2'}" exact>Page2</router-link>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.router-link-active {
  color:green;
}
</style>
