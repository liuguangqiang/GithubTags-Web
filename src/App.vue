<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'app'
  }
</script>

<style>
  body{
    padding: 0px;
    margin: 0px;
  }

  ul li{
    list-style-type:none;
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
  }

  #top-bar {
    background: #000;
    height: 60px;
  }

  .container{
    padding-left: 16px;
  }
</style>
