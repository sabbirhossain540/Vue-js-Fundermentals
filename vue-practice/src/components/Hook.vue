<template>
	<div class="Hook">
		<h1>{{ title }}</h1>
		<button @click="ChangeTitle">Click Me</button>
	</div>
	
</template>

<script>

	export default {
		name: 'Hook',
		data(){
			return {
				title: 'Hook main data'
			}
		},
		methods:{
			ChangeTitle(){
				this.title = 'Hook Updated Data'
			}
		},
		beforeCreate(){
				alert("Before Accelarated Hook")
		},
		created(){
				alert("Created Hook")
		},
		beforeUpdate(){
			alert("Before update Accelarated Hook")
		}
	}

</script>

<style scoped>

	
</style>