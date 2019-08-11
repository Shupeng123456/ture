<template>
	<div>
		<location-Header></location-Header>
		<location-List></location-List>
	</div>
</template>

<script>
	import locationHeader from './components/locationHeader'
	import locationList from './components/locationList'
	export default{
		name:'Location',
		components:{
			locationHeader,
			locationList
		}
	}
</script>

<style>
</style>