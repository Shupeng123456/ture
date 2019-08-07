<template>
 <div>
  <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for="item of swiperSlides" :key="item.id">
    	<img :src='item.imgurl' class="slide" />
    </swiper-slide>
  
  
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
   
  </swiper>
 </div>
</template>

<script>
	export default{
		name:"homeSwiper",
		data(){
			return{
				
				swiperOption:{
					 pagination:'.swiper-pagination',
					 loop:true,
					 autoplay: 3000,
                      speed: 1000,
                      
				},
				swiperSlides:[
				{
				 imgurl:'https://pic5.40017.cn/03/000/d5/6b/rB5oQFx4846ATjD9AAMGEUvrZHQ915_520x218_00.jpg',
				 id:'001'
				},
				{
				 
				 imgurl:'https://pic5.40017.cn/03/000/28/73/rB5oQFxG7M2AOgxwAADChAKgVcA559_520x218_00.jpg',
				 id:'002'
				}
			  ]
			}
		}
	}
</script>

<style lang='stylus' scoped>
.wr >>> .swiper-pagination-bullet
  background:#fff
.slide
  width:100%
</style>