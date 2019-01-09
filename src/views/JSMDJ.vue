<template>
	<div>
<form>
	<div class="form-group">
		<label>Email address</label>
		<input type="text" class="form-control"  v-model="email"  placeholder="Enter email">
		<label>Password</label>
        <input type="text" class="form-control" v-model="password" placeholder="Enter Password">
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
			earr:[],
			password:"",
			parr:[]
		}
	},
	created(){
    this.earr=JSON.parse(localStorage.getItem('id')) || [];
    this.parr=JSON.parse(localStorage.getItem('id1')) || [];
	},
	methods:{
		setValue(){
            this.earr.push(this.email);
            this.parr.push(this.password);
            localStorage.setItem('id',JSON.stringify(this.earr));
            localStorage.setItem('id1',JSON.stringify(this.parr));
		}
	}
}
</script>

<style>
</style>

