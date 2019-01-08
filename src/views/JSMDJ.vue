<template>
	<div>
<form>
	<div class="form-group">
		<label>Email address</label>
		<input type="text" class="form-control"  v-model="email"  placeholder="Enter email">

	</div>
	<router-link to="/Display"><button type="submit" class="btn btn-primary" @click="setValue">Submit</button></router-link>
</form>
<!-- <h6 v-for="earr1 in earr">{{earr1}}</h6> -->
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
	},
	methods:{
		setValue(){
            this.earr.push(this.email);
            localStorage.setItem('id',JSON.stringify(this.earr));
		}
	}
}
</script>

<style>
</style>

