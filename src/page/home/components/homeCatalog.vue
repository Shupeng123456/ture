<template>
	<div class="catalog">
		<div class="icon"
			 v-for='itme of iconList'
			 :key='itme.id'
			 >
			<div class="icon-img" >
				<img class="img" :class="[itme.color]" :src="itme.imgUrl">
			</div>
			<div class="icon-doce">{{itme.desc}}</div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'homeCatalog',
		props:{
			iconList:{Array}
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