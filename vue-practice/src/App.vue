<template>
  <div id="app">
    <h2>{{ title }}</h2>
    <navbar></navbar>
    <Hook></Hook>

  <!--  <AllFriends :friends="friends" @delete="deleteFriend"></AllFriends>

    <OnlineFriends :friends="friends"></OnlineFriends> -->

  </div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import Hook from './components/Hook.vue'

//import AllFriends from './components/AllFriends.vue'

//import OnlineFriends from './components/OnlineFriends.vue'

export default {
  name: 'App',
  data(){
    return {
      title : 'Wow Our View Website are Running',
      // friends: [
      //     { name: 'A', online: true},
      //     { name: 'B', online: false},
      //     { name: 'C', online: true},
      //     { name: 'D', online: false},
      //     { name: 'E', online: false},
      //     { name: 'F', online: true}
      //   ]
    }
  },
  components:{
   // Navbar, AllFriends, OnlineFriends
   Navbar, Hook
  },
  methods:{
    // deleteFriend(payload){
    //   //console.log(payload)
    //   this.friends = this.friends.filter(friend => {
    //     return friend.name !==payload.name
    //   })
    // }
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
