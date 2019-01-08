<template>
	<div>
<h6 v-for="earr1 in earr">{{earr1}}</h6>
</div>
</template>

<script>
export default{
	data:function(){
		return{
			email:"",
			earr:[]
		}
	},
	created(){
    this.earr=JSON.parse(localStorage.getItem('id'));
	}
}
</script>

<style>
</style>

