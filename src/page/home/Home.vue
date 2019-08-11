<template>
   <div class="home">
   <home-Header class="home-header" :city="city"></home-Header>
	<home-Swiper :swiperList="swiperList"></home-Swiper>
	<home-Catalog :iconList="iconList"></home-Catalog>
	<home-Hot 
		:hotContentList="hotContentList"
		:hotPriseList="hotPriseList"
		:hotTrendList="hotTrendList"
		></home-Hot>
	<home-Weekend :weekendList="weekendList"></home-Weekend>
	<home-Guess :guessList="guessList"></home-Guess>
    </div>
	
</template>

<script>
  import axios from 'axios'
  import homeHeader from './components/homeHeader'
  import homeSwiper from './components/homeSwiper'
  import homeCatalog from './components/homeCatalog'
   import homeHot from './components/homeHot'
   import homeWeekend from './components/homeWeekend'
    import homeGuess from './components/homeGuess'
	export default{		
		name:'Home',
		data(){
			return{
				city:'',
				guessList:'',
				hotContentList:'',
				hotPriseList:'',
				hotTrendList:'',
				iconList:'',
				swiperList:'',
				weekendList:''
			}
		},
		components:{
			homeHeader,
			homeSwiper,
			homeCatalog,
			homeHot,
			homeWeekend,
			homeGuess
		},
		methods:{
			getHomeData(){
				axios.get("/api/index.json")
				     .then(this.getHomeDataSucc)
				
			},
			getHomeDataSucc(res){
				const rel=res.data;
				const data=rel.data
				if(data){
					this.city=data.city
				this.guessList=data.guessList
				this.hotContentList=data.hotContentList
				this.hotPriseList=data.hotPriseList
				this.hotTrendList=data.hotTrendList
				this.iconList=data.iconList
				this.swiperList=data.swiperList
				this.weekendList=data.weekendList
				console.log(data)
				}
				
				
			}
		},
		mounted(){
			this.getHomeData()
			
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