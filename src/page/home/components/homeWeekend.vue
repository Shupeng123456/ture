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
		data(){
			return{
				swiperOption:{
					freeMode:true,
					spaceBetween:20,
					 slidesPerView: 3
					 
				},
				weekendList:[
        {
          "id":"0001",
          "imgUrl":"https://pic5.40017.cn/02/000/33/66/rBLkCFs0Tr6AXiFPAABmgwDtp7o002_280x190_00.jpg",
          "desc":"拈花湾",
          "detail":"禅意假日 古韵风光"

        },
        {
          "id":"0002",
          "imgUrl":"https://pic5.40017.cn/01/000/00/9c/rBANC1vD9_GAb2qVAAD1zTnOfl0327_280x190_00.jpg",
          "desc":"迪士尼",
          "detail":"点亮心中奇梦"
        },
        {
          "id":"0003",
          "imgUrl":"https://pic5.40017.cn/01/001/f8/b2/rBLkBlsWe--AYOxAAABvztYw1fM559_280x190_00.jpg",
          "desc":"东方盐湖城 · 道天下",
          "detail":"茅山脚下的逍遥山镇"
        },
        {
          "id":"0004",
          "imgUrl":"https://pic5.40017.cn/02/000/f8/b9/rBLkCFsWfOSAKWiGAABRaPAf0aA516_280x190_00.jpg",
          "desc":"天目湖",
          "detail":" 肆意山水 古街温泉 "
        },
        {
          "id":"0005",
          "imgUrl":"https://pic5.40017.cn/01/001/f8/b2/rBLkBlsWe--AYOxAAABvztYw1fM559_280x190_00.jpg",
          "desc":"揭阳湖",
          "detail":"山水人间 肆意快活"
        },
        {
          "id":"0006",
          "imgUrl":"https://pic5.40017.cn/02/000/f8/b9/rBLkCFsWfOSAKWiGAABRaPAf0aA516_280x190_00.jpg",
          "desc":"天目湖",
          "detail":"竹海 山水 温泉 古街"
        }
      ]
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