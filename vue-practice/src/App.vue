<template>
  <div id="app">
    <h2>{{ title }}</h2>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      title : 'Wow Our View Website are Running'
    }
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
