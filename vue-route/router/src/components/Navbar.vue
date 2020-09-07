<template>
	<div>
		<nav>
			<ul>
				<li><router-link to="/">Home</router-link></li>
				<li><router-link to="/about">About</router-link></li>
				<li><router-link to="/contact">Contact</router-link></li>
			</ul>
		</nav>


		<div>
			<ul>
				<li v-for="(id, index) in userIds" :key="index">
					<router-link :to="{name: 'Profile', params:{user_id:id}}">Profile {{ id }}</router-link>
				</li>
			</ul>

			<button @click="Contact">Contact</button>

			<button @click="About">Contact</button>
		</div>
		
	</div>
</template>

<script>

	export default {
		name: 'Navbar',
		data(){
			return {
				userIds : ['1','2','3','4','5','7']
			}
		},
		methods: {
			Contact(){
				this.$router.push({name: 'Contact'})
			},

			About(){
				this.$router.push({name: 'About'})
			}
		}
	}

</script>

<style scoped>
	nav{
		text-align: center;
	}

	nav ul{
		padding: 0;
	}
	nav li{
		display: inline-block;
		list-style-type: none;
		margin: 0;
		padding: 8px;
	}
	
</style>