<template>
	<div>
		<!-- <h1 class="text-danger">JSMPJ</h1> -->
		<form>
			<div class="form-group">
				<label for="exampleInputEmail1">Email address</label>
				<input type="text" class="form-control" id="exampleInputEmail1" v-model="guestName"  placeholder="Enter email">
			</div>
			<button type="submit" class="btn btn-primary" @click="saveGuest">Submit</button>
		</form>
	</div>
</template>

<script>

	
	export default{
		data:function(){
         return{
           guestName:"",
           myGuest:[]
         }
		},
	     created(){
          this.myGuest=JSON.parse(localStorage.getItem('keyy')) || [];


          },
		methods:{
			saveGuest(){
				this.myGuest.push(this.guestName); 

                localStorage.setItem('keyy', JSON.stringify(this.myGuest));
			}
		}
	}
</script>