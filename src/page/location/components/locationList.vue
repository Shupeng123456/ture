<template>
	<div class="list" ref="wrapper">
		<div >
		<div class="list-top">
			<div class="top-content">当前</div>
			<div class="top-bottom">正在获取位置信息</div>
		</div>
	    <div class="list-city">
	    	<div class="city">热门城市</div>
	    	<div class="city-choice">
	    		<ul>
	    			<li 
	    				v-for="item of hotCities"
	    				:key='item.id'
	    				>{{item.name}}</li>
	    		</ul>
	    		
	    	</div>
	    </div>
	    <div class="list-name" 
	    	v-for="(item,key) of cities" 
	    	:key="key">
	    	<h3>{{key}}</h3>
	    	<ul>
	    		<li v-for="inneritem of item">{{inneritem.name}}</li>
	    	</ul>
	    </div>
	    </div>
	</div>
</template>

<script>
	import BScroll from 'better-scroll'
	export default{
		name:'locationList',
		data(){
			return{
				hotCities:[
				{
					"id": 1,
			        "name": "北京"
				},
				{
					"id": 2,
			        "name": "北京"
				},
				{
					"id": 3,
			        "name": "北京"
				},
				{
					"id": 4,
			        "name": "北京"
				},
				{
					"id": 5,
			        "name": "北京"
				},
				{
					"id": 6,
			        "name": "北京"
				},{
					"id": 7,
			        "name": "北京"
				}],
				cities:{
				'A':[{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				     "spell": "aba",
				     "name": "阿坝"
				}
				],
				'B':[{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				     "spell": "aba",
				     "name": "阿坝"
				}
				],
				'C':[{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				      "spell": "aba",
				     "name": "阿坝"
				},
				{
					 "id": 56,
				     "spell": "aba",
				     "name": "阿坝"
				}
				]
				}
			}
		},
		mounted(){
			let scroll = new BScroll(this.$refs.wrapper)
		}
	}
</script>
 
<style lang="stylus" scoped>
.list
  background:#e9ecf1
  padding-top:.4rem
  width:100%
  height:12.14rem
  overflow:hidden
  .top-content,.city,h3
   margin-left:.4rem
   padding:.2rem 0
  .top-bottom,.city-choice li,.list-name li
    background:#fff
    padding.2rem .2rem
    line-height:.44rem
  .top-bottom
   width:84%
   margin-left:.2rem
 .list-city
  margin-top:.2rem
  overflow:hidden
  .city-choice li
   width:15%
   float:left
   margin:0 0 .2rem .2rem
   text-align:center
</style>