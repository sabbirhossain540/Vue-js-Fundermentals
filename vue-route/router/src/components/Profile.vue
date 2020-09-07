<template>
  <div class="profile">
    <h2>Profile Page</h2>
    {{ UserId }}
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
      UserId : this.$route.params.user_id
    }
  },
  methods: {
    updateId(){
      this.UserId = this.$route.params.user_id
    }
  },

  watch: {
    $route: 'updateId'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h2{
    color:green;
  }
</style>
