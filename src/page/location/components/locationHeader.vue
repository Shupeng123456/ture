<template>
	<div class="location">
		<span class="iconfont">&#xe615;</span>
	    <input type="text" placeholder="请输入城市名称（如北京、bj、beijing）" class="location-text"/>
	</div>
</template>

<script>
	export default{
		name:'locationHeader'
	}
</script>

<style lang="stylus" scoped>
	.location
	 height:.78rem
	 background:#e0e4ec
	 padding:.2rem
	 position:relative
	 .location-text
	  height:.78rem
	  line-height:.78rem
	  width:90%
	  padding-left:10%
	 .iconfont
	  position:absolute
	  top:.45rem
	  left:.4rem
</style>