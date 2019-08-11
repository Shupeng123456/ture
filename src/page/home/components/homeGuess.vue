<template>
	<div class="guess">
		<div class="guess-dace" :class="[guessfined]">
		    <div class="dace-top">猜你喜欢</div>
		</div>
		<div class="guess-content" 
			v-for="itme of guessList"
			:key="itme.id"
			>
		    <div class="content-img">
		    	<img :src="itme.imgUrl">
		    	<div class="content-dace">{{itme.crite}}</div>
		    </div>
		    <div class="content-pard">{{itme.desc}}</div>
		    <div class="content-dace">
		    	<div class="content-dace-top">酒店距景点<span>{{itme.distance}}</span>km</div>
		    	
		    	<div class="content-dace-bottom" >￥<span>{{itme.prise}}</span><span class="botton-span">起</span></div>
		    </div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'homeGuess',
		props:{
			guessList:{Array}
		},
		data(){
			return{
				guessfined:''
			}
		},
		methods:{
			scrollChange(){
				let scrollTop = document.documentElement.scrollTop;
				 if(scrollTop>600){
				 	this.guessfined='guesslont'
				 }else{
				 	this.guessfined=''
				 }
			}
		},
		mounted:function(){
			window.addEventListener("scroll",this.scrollChange)
		}
	}
</script>

<style lang="stylus" scoped>
	.guess
	 overflow:hidden
	 padding-top:.2rem
	 border-top: 0.2rem solid #eee;  
	 .guesslont
	  position:fixed
	  top:.9rem	
	  z-index:100
	  background:#fff
	 .guess-dace
	  overflow:hidden
	  height:0
	  width:100%
	  padding-bottom:12%
	  text-align: center
	  color:#23beae
	  .dace-top
	   overflow:hidden
	   height:0
	   padding-bottom:6%
	   font-weight:bold
	   width:20%;
	   margin:0 auto
	   padding-top:.35rem;
	   border-bottom:.1rem solid #23beae
	 .guess-content
	   border-top: 0.05rem #eee solid
	   overflow:hidden
	   height:0
	   padding-top:5%
	   padding-bottom:70%
	   width:94%
	   margin:0 auto
	   .content-img
	     overflow:hidden
	     height:0
	     padding-bottom:50%
	     position:relative
	     div
	      position:absolute
	      left:0
	      bottom:0
	      color:#fff
	     img
	      width:100%
	    .content-pard
	     font-weight:bold
	     padding-top:.09rem   
	    .content-dace
	     display:flex
	     justify-content:space-between
	     padding-top:.2rem
	     .content-dace-top
	      color:#ccc
	     .content-dace-bottom
	      color:red
	      .botton-span
	       color:black
	     
	      
</style>