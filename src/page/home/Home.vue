<template>
   <div class="home">
   <home-Header class="home-header"></home-Header>
	<home-Swiper></home-Swiper>
	<home-Catalog></home-Catalog>
	<home-Hot></home-Hot>
    </div>
	
</template>

<script>
  import homeHeader from './components/homeHeader'
  import homeSwiper from './components/homeSwiper'
  import homeCatalog from './components/homeCatalog'
   import homeHot from './components/homeHot'
	export default{		
		name:'Home',
		components:{
			homeHeader,
			homeSwiper,
			homeCatalog,
			homeHot
		}
	}
</script>

<style lang='stylus'>
   .home
     position:relative
     .home-header
       position:absolute
       width:100%
       z-index:100
</style>