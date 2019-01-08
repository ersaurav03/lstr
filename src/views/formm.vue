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
	const STORAGE_KEY = "guest-storage"
	
	export default{
		data:function(){
         return{
           guestName:"",
           myGuest:[]
         }
		},
	     created(){
          this.myGuest=JSON.parse(localStorage.getItem(STORAGE_KEY || '[]'))

          },
		methods:{
			saveGuest(){
				this.myGuest.push({
                guestName: this.guestName
                }) 

                this.guestName=""

                localStorage.setItem(STORAGE_KEY, JSON.stringify(this.myGuest));
			}
		}
	}
</script>