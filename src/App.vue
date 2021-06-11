<template>
  <div id="app">
    <div class="container">
      <img alt="Vue logo" src="./assets/logo.png" style="height: 120px;margin-top: 20%">
      <div class="row">
        <div class="col-12">
          <p>
            Test Drag and drop List
          </p>
        </div>
      </div>
      <HelloWorld msg="Welcome to Your Vue.js App" class="mt-5"/>
    </div>
  </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'

    export default {
        name: 'App',
        components: {
            HelloWorld
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
    min-height: 2500px;
  }
</style>
