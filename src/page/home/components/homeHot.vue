<template>
	<div class="hot">
		<div class="hot-left" >
			<div class="left-top">
				<div class="top-content">
					限时抢购
				</div>
				<div class="top-desc">
					距结束 <span>02</span>:<span>28</span>:<span>32</span>
				</div>
			</div>
			<div class="left-center" 
				v-for="itme of hotContentList"
			     :key="itme.id"
				>
				<div class="center-img">
					<img :src="itme.imgUrl" />
				</div>
				<div class="center-desc">
					{{itme.desc}}
				</div>
		    </div>
			<div class="left-bottom"
				v-for="itme of hotPriseList"
			     :key="itme.id"
				>
				<div class="bottom-left">
					限量<span>{{itme.num}}</span>份
				</div>
				<div class="bottom-right">
					<span>￥</span><span class="big">{{itme.prise}}</span>起
				</div>
			</div>
		</div>
		
		<div class="hot-right">
			<div class="right-top" 
				v-for="itme of hotTrendList"
				:key="itme.id"
				>
				<div class="top-left">
					{{itme.desc}}
					<p>{{itme.crite}}</p>
				</div>
				<div class="top-right">
					<img :src="itme.imgUrl" />
				</div>
			</div>
			
		</div>
	</div>
	

</template>

<script>
	export default{
		name:'homeHot',
		props:{
		 hotContentList:{Array},
		 hotPriseList:{Array},
		 hotTrendList:{Array}
		}
	}
</script>

<style lang="stylus" scoped>
 @import '../../../assets/style/mixins.styl'
	.hot
	 width:100%
	 overflow:hidden
	 border-top:.2rem solid #eee
	 .hot-left
	  float:left
	  overflow:hidden
	  width:50% 
	  padding:.075rem
	  .left-top
	   width:100%
	   overflow:hidden
	   padding:.07rem 0 .1rem 0   
	   .top-content
	    float:left
	    color:red
	    font-weight:bold
	   .top-desc
	    float:right
	    span
	     background:black
	     color:#fff
	     display:inline-block
	     border-radius:.02rem
	  .left-center
	   display:flex
	   overflow:hidden
	   width:100%
	   .center-img
	    width:30.7%
	    img
	     width:100%   
	   .center-desc
	    width:68.3%
	    overflow:hidden
	    margin-left:.2rem
	    ellipsis() 
	    line-height:.4rem
	  .left-bottom
	   width:100%;
	   overflow:hidden;
	   display:flex;	   
	   justify-content:space-between;
	   padding:.07rem 0 .09rem 0;
	   .bottom-right
	    span
	     color:red
	    .big
	     display:inline-block
	     font-weight:bold
	     font-size:.4rem
	    
	    
	   
	 .hot-right
	  float:right 
	  overflow:hidden
	  width:46%
	  border-left:.05rem solid #eee
	  .right-top
	   display:flex
	   overflow:hidden
	   width:100%
	   justify-content:space-around
	   border-bottom:.03rem #eee solid
	   .top-left
	    font-weight:bold
	    padding-top:.15rem
	    overflow:hidden
	    width:50%
	    p
	     color:#ccc
	     padding-top:.3rem
	     overflow:hidden
	     text-overflow:ellipsis
	     white-space:nowrap 
	   .top-right
	    width:1.1rem
	    img
	     width:1.1rem  
 
</style>
