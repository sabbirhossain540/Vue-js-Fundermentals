<template>
  <div class="home">
    <h2>Home Page</h2>
    <p>{{ title }}</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
     	title:'Welcome to vue js fundermentals'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
