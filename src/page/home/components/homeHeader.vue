<template>
	<div class='header' :class="[scrolltop]">
		<div class="header-back">
			<span class="iconfont">&#xe641;</span>
		</div>
		<div class="header-search" :class=[scrollcontent]>上海翠湖公园<span class="iconfont">&#xe615;</span></div>
		<div class="header-city ">北京<span class="iconfont">&#xe65d;</span></div>
	</div>
</template>

<script>
	export default{
		name:"homeHeader",
		data(){
			return{
				scrolltop:'',
				scrollcontent:''
			}
		},
		methods:{
			scrollguand(){
				let height=document.documentElement.scrollTop
				if(height>50){
					this.scrolltop='scrolltops'
					this.scrollcontent='scrollcontents'
				}else{
					this.scrolltop=''
					this.scrollcontent=''
				}
			}
		},
		mounted(){
			window.addEventListener("scroll",this.scrollguand)
		}
	}
</script>

<style lang='stylus' scoped>
    .scrolltops
     position:fixed  
     background:#fff
	.header
	  line-height:.88rem
	  text-align:center
	  display:flex
	 .header-back
	    float:left
	    width:.9rem
	 .header-search
	   flex:1
	   height:.64rem
	   line-height:.6rem
	   margin-top:.2rem
	   margin-left:.2rem
	   margin-right:.2rem
	   border-radius:.5rem
	   box-shadow:0 0 .01rem .01rem #fff;
	  .scrollcontents
	   background:#eee
	   color:#aaa
	 .header-city
	    float:right
	    width:1.4rem
	  
</style>