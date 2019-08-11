<template>
	<div class="weekend">
		<div class="weekend-header">
			<div class="header-dace">
				///////<span>周末出游</span>//////
			<p>致力推荐超完美套餐</p>
			</div>
		</div>
		<div class="weenkend-dace">
		  <swiper :options="swiperOption" >
               <swiper-slide
               	 v-for="itme of weekendList"
               		:key="itme.id"
               		>
               	<div class="swiper-content" >
    	          <div class="swiper-img">
    	          	<img :src="itme.imgUrl">
    	          </div>
    	          <div class="swiper-dace">
    	          	{{itme.desc}}
    	          	<p>{{itme.detail}}</p>
    	          </div>
    	        </div>
               </swiper-slide>
           </swiper>
		</div>
	</div>
</template>

<script>
	export default{
		name:'homeWeekend',
		props:{
			weekendList:{Array}
		},
		data(){
			return{
				swiperOption:{
					freeMode:true,
					spaceBetween:20,
					 slidesPerView: 3
					 
				},
		
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.weekend
	 overflow:hidden
	 height:0
	 padding-bottom:55%
	 border-top: 0.2rem solid #ee
	 margin-top:0.2rem
	 .weekend-header
	  overflow:hidden
	  height:0
	  padding-bottom:15.5%
	  text-align:center
	  
	  position:relative
	  .header-dace
	   position:absolute
	   top:50%
	   left:50%
	   transform: translate(-50%, -50%)
	   color:#aaa
	   span
	    color:black
	   p
	    padding-top:5% 
	 .weenkend-dace
	  overflow:hidden
	  height:0
	  padding-bottom:84.5%
	  
	  .swiper-content
	   overflow:hidden
	   width:100%
	   height:0
	   padding-bottom:120%
	   border:1px solid #ccc
	   display:inline-block
	   margin-left:15%
	   .swiper-img
	    overflow:hidden
	    height:0
	    padding-bottom:68%
	    img
	     max-width:100%
	  .swiper-dace
	   overflow:hidden
	   text-overflow:ellipsis
	   white-space:nowrap 
	   font-weight:bold
	   color:#000
	   text-align:center
	   padding-top:.2rem       
	   p
	    margin-top:.15rem
	    color:#ccc
	    overflow:hidden
	    text-overflow:ellipsis
	    white-space:nowrap 
	    
	   
</style>