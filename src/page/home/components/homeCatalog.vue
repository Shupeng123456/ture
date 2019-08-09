<template>
	<div class="catalog">
		<div class="icon"
			 v-for='itme of iconlist'
			 :key='itme.id'
			 >
			<div class="icon-img" >
				<img class="img" :class="[itme.color]" :src="itme.imgulr">
			</div>
			<div class="icon-doce">{{itme.decu}}</div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'homeCatalog',
		data(){
			return{
			iconlist:[
			{
				id:'001',
				imgulr:'https://pic5.40017.cn/01/000/84/4f/rBLkBVmLtaiAcmRaAAAEH9JbM6g234.png',
				decu:'本地热推',
				color:'red'
			},
			{
				id:'002',
				imgulr:'https://pic5.40017.cn/02/001/6d/e2/rBLkCFmEG8eALBI8AAAEA1xXmqI793.png',
				decu:'亲子游',
				color:'green'
			},
			{
				id:'003',
				imgulr:'https://pic5.40017.cn/02/001/6d/db/rBLkCVmEGfeAVI4FAAAEXdabEDE534.png',
				decu:'温泉预售',
				color:'blue'
			},
			{
				id:'004',
				imgulr:'https://pic5.40017.cn/02/001/6d/e2/rBLkCFmEG8eALBI8AAAEA1xXmqI793.png',
				decu:'自然风光',
				color:'pink'
			}
			]
		}
		}
	}
</script>

<style lang="stylus" scoped>
.catalog
  margin-top:.19rem
  margin-bottom:.2rem
  overflow:hidden
.icon
   width:25%
   text-align:center
   float:left
   .img
     width:50%
     border-radius:1rem
   .icon-doce
     padding-top:.12rem  
.red
  background:red
.green
  background:green
.blue
  background:blue    
.pink
  background:pink   
   
  
</style>