<template>
	<div>
<h6 v-for="earr1 in earr">{{earr1}}</h6>
<h6 v-for="parr1 in parr">{{parr1}}</h6>
</div>
</template>

<script>
export default{
	data:function(){
		return{
			email:"",
			earr:[],
			password:"",
			parr:[]
		}
	},
	created(){
    this.earr=JSON.parse(localStorage.getItem('id')) || [];
    this.parr=JSON.parse(localStorage.getItem('id1')) || [];

	}
}
</script>

<style>
</style>

