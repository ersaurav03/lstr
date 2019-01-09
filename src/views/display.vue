<template>
	<div>
		<table>
			<thead>
<!-- 				<tr>
					<th>ID</th><th>Password</th>
				</tr> -->
			</thead>
			<tbody>
			<tr>
				<td>
				<th scope="row">Email</th>
				<tr v-for="earr1 in earr">{{earr1}}</tr>
			</td>
			
			
				<td>
				<th scope="row">Passworrd</th> 
				<tr v-for=" parr1 in parr">{{parr1}}</tr>
				</td>
			</tr>
			</tbody>
		</table>
<!-- ID's<h6 v-for="earr1 in earr">{{earr1}}</h6>
Password's:<h6 v-for="parr1 in parr">{{parr1}}</h6> -->
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

