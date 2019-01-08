<template>
	<div>
		<form>
			<div class="form-group">
				<label for="exampleInputEmail1">Email address</label>
				<input type="text" class="form-control" id="exampleInputEmail1" v-model="email"  placeholder="Enter email">
					<label for="exampleInputPassword1">Password</label>
				<input type="password" class="form-control" id="exampleInputPassword1" v-model="password" placeholder="Password">
				
			</div>
			<button type="submit" class="btn btn-primary" @click="saveGuest">Submit</button>
		</form>
	</div>
</template>

<script>
	export default{
		data:function(){
         return{
            email:"",
            password:"",
         	earr:[],
            parr:[]             
         }
		},
	     created(){
          this.earr=JSON.parse(localStorage.getItem('e_arr'));
          this.parr=JSON.parse(localStorage.getItem('p_arr'));
          },
		methods:{
			saveGuest(){
				this.earr.push(this.email) ;
                this.parr.push(this.password);
                
                localStorage.setItem('p_arr', JSON.stringify(this.parr));
                localStorage.setItem('e_arr', JSON.stringify(this.earr));
			}
		}
	}
</script>