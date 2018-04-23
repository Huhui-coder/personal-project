<template>
    <div>
    	 <div class="palace">
			 <img src="./assets/images/i.png" alt=""><span>重庆市</span>
			 <div class="fr">
			 <span>分享</span>
			<span>编辑</span>
             </div>
		 </div>
		 <div class="content-wrap">
		 <div class="content">
			 <span class="name">春秋文化图书专营店> </span>
			 <span class="fr"> 去凑单></span>
		 </div>
		 <div class="book">
			 <img src="./fixtures/covers/2.svg" alt="">
			 <div class="desc">
			 <span>安卓开发实战</span>
			 <span>你值得拥有</span>
			 </div>
			 <div class="count">
               <div>
				   <span>
					   <button @click="conutdel">-</button>
				   </span>
				   <span>
					   <input type="text" v-model="count">
				   </span>
				   <span>
					   <button @click="conutadd">+</button>
				   </span>
			   </div>
			 </div>
			 <div class="price">
				 ￥{{total}}
			 </div>
			 <div class="btn">
购买			 </div>
		 </div>
		 </div>
		 		 <div class="content-wrap">
		 <div class="content">
			 <span class="name">春秋文化图书专营店> </span>
			 <span class="fr"> 去凑单></span>
		 </div>
		 <div class="book">
			 <img src="./fixtures/covers/1.svg" alt="">
			 <div class="desc">
			 <span>大数据实战</span>
			 <span>你值得拥有</span>
			 </div>
			  <div class="count">
               <div>
				   <span>
					   <button @click="conutdel">-</button>
				   </span>
				   <span>
					   <input type="text" v-model="count">
				   </span>
				   <span>
					   <button @click="conutadd">+</button>
				   </span>
			   </div>
			 </div>
			 <div class="price">
				 ￥{{total}}
			 </div>
			 <div class="btn">
购买			 </div>
		 </div>
		 </div>
		 
    </div>
</template>
<style>
body{
	background-color: white;
	font-family: 'Times New Roman', Times, serif;
}
   span i{
	   width: 0;
	   height: 0;
	   border: 1px solid  sienna;
   }
   span{
	   font-family:'Times New Roman', Times, serif
   }
   .content .fr{
	   float: right;
   }
   .fr span{
	   margin-right: 15px;
	   color:peru;
   }
   .palace{
	   padding: 10px;
	   border-bottom: 1px solid rgba(172, 161, 161,.5);
   }
   .content-wrap {
	   margin-top: 16px;
	   width: 100%;
	   height: 240px;
	   position: relative;
	   margin-bottom: 1px;
	   background-color: rgba(247, 242, 247, 0.3);
	   border-bottom: 1px solid  rgba(80, 10, 10, 0.9);
	   border-radius: 18px;
   }
   .content{
	   width: 100%;
	   height: 16px;
   }
   .book{
	   width: 98%;
		  position: absolute;
		  top: 35px;	
		  border: 1px solid  rgba(172, 161, 161,.5);  
   }
   .book .desc{
position: absolute;
top: 56px;
left: 189px;
width: 186px;	 
color: #000000;
   } 
   .book .price{
position: absolute;
top: 139px;
left: 230px;
width: 186px;
font-size: 18px;	
   }
      .book .btn{
		  color: tomato;
		font-size: 17px;
		border: 1px solid #000000;
  position: absolute;
   top: 132px;
   left: 286px;
   padding: 5px;
   border-radius: 6px;
   }
   .count{
	   position: absolute;
	   
	   
   }
   .count button{
	   width: 35px;
	   	   height: 35px;

	   background-color:rgba(172, 161, 161,.3);
   }
   .count input{
	   width: 35px;
			  height: 35px;
			  border: none;
			  text-align: center;
	   background-color:rgba(172, 161, 161,.3);
 }
</style>
<script type="text/ecmascript-6">
    export default{
    	data (){
    		return {
    			storeKey:"VUE-CART",
				items:[],
				total:56,
				count:1
    		}
    	},
    	computed: {
    		is_empty () {
    			return this.items == undefined || this.items.length == 0
    		}
    	},
    	created () {
    		if (localStorage[this.storeKey]!=undefined) {
    			this.items =JSON.parse(localStorage[this.storeKey])
    		}
    	},
    	mehtods: {
    		saveStore () {
    			localStorage.setItem(this.storeKey,JSON.stringify(this.items))
    		},
    		checkout() {
			},
			conutdel(){
				this.count--;
			},
			conutadd(){
				this.count++;
			},
    	}
    }
</script>