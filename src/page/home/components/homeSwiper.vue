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
				 imgurl:'../../../../static/img/2015.png',
				 id:'001'
				},
				{
				 
				 imgurl:'../../../../static/img/2015.png',
				 id:'002'
				}
			  ]
			}
		}
	}
</script>

<style lang='stylus' scoped>
.wr >>> .swiper-pagination-bullet
  background:#fff!important
.slide
  width:100%
</style>