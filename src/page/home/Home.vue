<template>
	<div class="text">home<home-Header></home-Header></div>
</template>

<script>
  import homeHeader from './components/homeHeader'
	export default{
		name:'Home',
		components:{
			homeHeader
		}
	}
</script>

<style lang='stylus'>
.text
  color:blue;
</style>