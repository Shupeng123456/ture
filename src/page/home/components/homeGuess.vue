<template>
	<div class="guess">
		<div class="guess-dace" :class="[guessfined]">
		    <div class="dace-top">猜你喜欢</div>
		</div>
		<div class="guess-content" 
			v-for="itme of guessList"
			:key="itme.id"
			>
		    <div class="content-img">
		    	<img :src="itme.imgUrl">
		    	<div class="content-dace">{{itme.crite}}</div>
		    </div>
		    <div class="content-pard">{{itme.desc}}</div>
		    <div class="content-dace">
		    	<div class="content-dace-top">酒店距景点<span>{{itme.distance}}</span>km</div>
		    	
		    	<div class="content-dace-bottom" >￥<span>{{itme.prise}}</span><span class="botton-span">起</span></div>
		    </div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'homeGuess',
		data(){
			return{
				guessfined:'',
				guessList:[
        {
          "id":"0002",
          "imgUrl":"https://pic5.40017.cn/02/000/be/ca/rBANDFnRm9yAIcKpAAd0bfhGxZk791_420x228_00.JPG",
          "crite":"148点评  70%满意度",
          "logo":"同城专属",
          "desc":"【近南山竹海】住安雲·悦南山度假酒店，自选天目湖南山竹海/山水园/御水温泉等【天目湖休闲游】",
          "distance":"1.34",
          "prise":"699"
        },
        {
          "id":"0004",
          "imgUrl":"https://pic3.40017.cn/zzy/rimage/2015/03/17/11/506Nl6_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"【引爆双早双晚399】扬州中集格兰云天大酒店+自选瘦西湖/个园/瘦西湖温泉+双人早餐",
          "distance":"1.34",
          "prise":"269"
        },
        {
          "id":"0005",
          "imgUrl":"https://pic3.40017.cn/zzy/rimage/2015/04/18/17/hETxTo_420x228_00.jpg",
          "crite":"8点评  100%满意度",
          "logo":"同城专属",
          "desc":"上海崇明东平国家森林公园房车1晚+森林公园门票2张+双人早餐",
          "distance":"7.00",
          "prise":"299"
        },
        {
          "id":"0006",
          "imgUrl":"https://pic5.40017.cn/02/000/02/22/rBLkCVlkdDqAP4NzAAMCZSYX5mY633_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"无锡拈花客栈1晚，游拈花湾，自选酒店自助晚餐/禅食餐【灵山胜境】【亲子精选】",
          "distance":"1.34",
          "prise":"289"
        },
        {
          "id":"0007",
          "imgUrl":"https://pic5.40017.cn/02/000/38/a9/rBANDFkpMDKAa0E2AAQAADJG_o4457_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"住横店旗下酒店1晚,自选横店影视城各景点、梦泉谷、梦幻谷(含演出)【横店2日游】",
          "distance":"34",
          "prise":"239"
        },
        {
          "id":"0008",
          "imgUrl":"https://pic3.40017.cn/zzy/rimage/2015/03/17/12/ua9Ic2_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"游黄山，自选景区内山顶酒店（北海/狮林/白云/西海/排云楼/光明顶）",
          "distance":"134",
          "prise":"249"
        },
        {
          "id":"0009",
          "imgUrl":"https://pic3.40017.cn/zzy/rimage/2015/03/26/20/qLpvQc_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"住宋城千古情主题酒店（杭州西湖店），自选杭州宋城千古情景区，预订套餐包含贵宾席演出票！",
          "distance":"14",
          "prise":"69"
        },
        {
          "id":"00010",
          "imgUrl":"https://pic5.40017.cn/01/001/31/a0/rBANC1vaeM6AAnKsAAC6cdvPNUE365_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"天目湖涵庭假日山庄，与友相聚、尽兴欢愉，山水园/涵田温泉等多套餐自选【精选度假酒店】",
          "distance":"34",
          "prise":"2669"
        },
        {
          "id":"00011",
          "imgUrl":"https://pic3.40017.cn/zzy/rimage/2015/03/24/17/oc97dU_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"住景区内西塘华源轩主题客栈，游西塘古镇，感受温柔淳朴的古镇韵味【错峰避人群、更优惠】",
          "distance":"14",
          "prise":"669"
        },
        {
          "id":"00012",
          "imgUrl":"https://pic5.40017.cn/02/000/2b/df/rBLkCFqTxOaAbkgzAAHHOxTJQLg483_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"【引爆双早双晚399】住扬州中集格兰云天大酒店+自选双人晚餐/瘦西湖温泉+双人早餐",
          "distance":"14",
          "prise":"399"
        },
      
        {
          "id":"00014",
          "imgUrl":"https://pic4.40017.cn/scenery/destination/2016/07/19/17/lziIen_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"常州明都枫泽山庄大酒店1晚，自选淹城野生动物园景点/常州明都枫泽山庄大酒店自助晚餐套餐",
          "distance":"14",
          "prise":"69"
        },
        {
          "id":"00015",
          "imgUrl":"https://pic5.40017.cn/02/000/54/fb/rBANDFtHJ3yAE7pWAAE0a3dx4Zo142_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"入住句容碧桂园凤凰城酒店+双份自助早餐+自选汤山一号温泉/颐尚温泉/紫清湖温泉",
          "distance":"14",
          "prise":"69"
        },
        {
          "id":"00016",
          "imgUrl":"https://pic4.40017.cn/scenery/destination/2017/02/08/18/ZTe8Qb_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"宿宜兴帕佛伦斯酒店，自选宜兴竹海风景区等，尊享60楼“云端”自助早餐，免费泳池健身房【亲子精选】",
          "distance":"154",
          "prise":"629"
        },
        {
          "id":"00018",
          "imgUrl":"https://pic4.40017.cn/scenery/destination/2017/01/23/17/XeJ3ph_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "logo":"同城专属",
          "desc":"住上海柏思特酒店，享儿童乐园，游上海迪士尼乐园【亲子精选】【亲子主题】",
          "distance":"14",
          "prise":"869"
        },
        {
          "id":"00019",
          "imgUrl":"https://pic4.40017.cn/zzy/rimage/2016/10/10/23/mVRN8E_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "desc":"常州恐龙主题度假酒店1晚+恐龙人俱乐部5选1，自选恐龙园景点门票或自助晚餐",
          "logo":"同城专属",
          "distance":"14",
          "prise":"269"
        },
        {
          "id":"00020",
          "imgUrl":"https://pic5.40017.cn/02/000/62/5a/rBANDFoFdVOAS6rOAAL2qonaRWU933_420x228_00.jpg",
          "crite":"18点评  100%满意度",
          "desc":"住无锡318文化大院，游灵山小镇拈花湾（相距约3公里）",
          "logo":"同城专属",
          "distance":"124",
          "prise":"649"
        }
      ]}
     },
		methods:{
			scrollChange(){
				let scrollTop = document.documentElement.scrollTop;
				 if(scrollTop>600){
				 	this.guessfined='guesslont'
				 }else{
				 	this.guessfined=''
				 }
			}
		},
		mounted:function(){
			window.addEventListener("scroll",this.scrollChange)
		}
	}
</script>

<style lang="stylus" scoped>
	.guess
	 overflow:hidden
	 padding-top:.2rem
	 border-top: 0.2rem solid #eee;  
	 .guesslont
	  position:fixed
	  top:.9rem	
	  z-index:100
	  background:#fff
	 .guess-dace
	  overflow:hidden
	  height:0
	  width:100%
	  padding-bottom:12%
	  text-align: center
	  color:#23beae
	  .dace-top
	   overflow:hidden
	   height:0
	   padding-bottom:6%
	   font-weight:bold
	   width:20%;
	   margin:0 auto
	   padding-top:.35rem;
	   border-bottom:.1rem solid #23beae
	 .guess-content
	   border-top: 0.05rem #eee solid
	   overflow:hidden
	   height:0
	   padding-top:5%
	   padding-bottom:70%
	   width:94%
	   margin:0 auto
	   .content-img
	     overflow:hidden
	     height:0
	     padding-bottom:50%
	     position:relative
	     div
	      position:absolute
	      left:0
	      bottom:0
	      color:#fff
	     img
	      width:100%
	    .content-pard
	     font-weight:bold
	     padding-top:.09rem   
	    .content-dace
	     display:flex
	     justify-content:space-between
	     padding-top:.2rem
	     .content-dace-top
	      color:#ccc
	     .content-dace-bottom
	      color:red
	      .botton-span
	       color:black
	     
	      
</style>