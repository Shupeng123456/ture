<template>
 <div>
  <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
    	<img :src='item.imgUrl' class="slide" />
    </swiper-slide>
  
  
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
   
  </swiper>
 </div>
</template>

<script>
	export default{
		name:"homeSwiper",
		props:{
			swiperList:{Array}
		},
		data(){
			return{
				
				swiperOption:{
					 pagination:'.swiper-pagination',
					 loop:true,
					 autoplay: 3000,
                      speed: 1000,
                      
				},
				
				
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