<template>
	<div class="Hook">
		<h1>Posts</h1><hr>	
		<div v-for="post in posts" :key="post.id">
			<h2>{{ post.title }}</h2>
			<p>{{ post.body | snipet }}</p>			
		</div>

	</div>
	
</template>

<script>
	import axios from 'axios'
	export default {
		name: 'Hook',
		data(){
			return {
				posts:[]
			}
		},
		methods:{
	
		},
		created(){
			axios.get('https://jsonplaceholder.typicode.com/posts')
			.then(response =>{
				console.log(response)
				this.posts = response.data
			})
			.catch(error=>{
				console.log(error)
			})
		}
	}

</script>

<style scoped>
h1{
	color: red;text-align: center;
}
table tr td {
	border-right: 1px solid black;
}
	
</style>