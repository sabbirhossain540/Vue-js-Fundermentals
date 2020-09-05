<template>
	<div id="allfriends">
		<h2>All Friends</h2>

		<div v-for="(friend,index) in friends" :key="index" >
			<h4 @click="unfriend(friend.name)"> {{ friend.name }} </h4>
		</div>
		
	</div>
</template>

<script>

	export default {
		name: 'AllFriends',
		props:['friends'],
		data(){
			return {
				
			}
		},
		methods:{
			unfriend(name){
				//console.log(name)
				this.$emit('delete',{name})
			}
		}
	}

</script>

<style scoped>

</style>