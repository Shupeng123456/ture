<template>
	<div class="hot">
		<div class="hot-left" 
			v-for="itme of hotlisc"
			:key="itme.id"
			>
			<div class="left-top">
				<div class="top-content">
					限时抢购
				</div>
				<div class="top-desc">
					距结束 <span>02</span>:<span>28</span>:<span>32</span>
				</div>
			</div>
			<div class="left-center">
				<div class="center-img">
					<img :src="itme.imgurl" />
				</div>
				<div class="center-desc">
					{{itme.dace}}
				</div>
		    </div>
			<div class="left-bottom">
				<div class="bottom-left">
					限量<span>{{itme.so}}</span>份
				</div>
				<div class="bottom-right">
					<span>￥</span><span class="big">{{itme.big}}</span>起
				</div>
			</div>
		</div>
		
		<div class="hot-right">
			<div class="right-top" 
				v-for="itme of hotTrendList"
				:key="itme.id"
				>
				<div class="top-left">
					{{itme.dace}}
					<p>{{itme.boar}}</p>
				</div>
				<div class="top-right">
					<img :src="itme.imgurl" />
				</div>
			</div>
			
		</div>
	</div>
	

</template>

<script>
	export default{
		name:'homeHot',
		data(){
			return {
				hotlisc:[
				{
					id:'001',
					imgurl:'https://pic5.40017.cn/01/000/9d/d9/rBLkBlmSl26AACtXAALg8QhHckM352_100x100_00.jpg',
					dace:'上海野生动物园成人票2张+上海浦东机场莎海国际酒店豪华双床房1晚',
					so:'100',
					big:'299'
				}],
				hotTrendList:[{
					id:'001',
					dace:'温泉爆款',
					boar:'又到一年温泉季',
					imgurl:'https://pic5.40017.cn/01/000/65/88/rBANC1usNjyAWsDJAACkawp55dU429_100x100_00.png'
				},
				{
					id:'002',
					dace:'温泉爆款',
					boar:'又到一年温泉季',
					imgurl:'https://pic5.40017.cn/01/000/65/88/rBANC1usNjyAWsDJAACkawp55dU429_100x100_00.png'
				}
				],
			}
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
	  width:47%
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
	    p
	     color:#ccc
	     padding-top:.3rem
	   .top-right
	    width:1.1rem
	    img
	     width:1.1rem  
 
</style>
