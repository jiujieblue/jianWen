<template>
	<div class="content">
	 	<BannerView>
	 	</BannerView>
	    <div class="newsList">
	      <ul>
	            <li v-for="(item,index) in homeData">
	            	<router-link to="/article">
	               
	                    <h2>{{item.title}}</h2>
	                    <p>{{item.detail}}</p>
	                </router-link>
	            </li>
	            
	        </ul>
	    </div>
	</div>
</template>
<script>
import BannerView from './Banner.vue'
export default{
	data(){
		return{
			homeData:[]
		}
	},
	mounted(){
		//获取数据
		this.getHomeData();
	},
	methods:{
		getHomeData(){
			var _this=this;
			this.$http.get('./src/data/index.data').then(function (res) {
				_this.homeData=res.data;
				console.log(res.data);
			}).catch(function(err){
				alert(' 请求数据失败'+err)
			});
		}
	},
	/*methods:{
		fetchData(){
			var _this=this;
			this.$http.get('src/data/index.data').then(function(res){
				//console.log( res.data);
				//setTimeout(function(){
					_this.arrList=res.data;
				//},1000);
			}).catch(function(err){
				console.log(err);
			});
		}
	},*/
	components:{
		BannerView
	}
}
</script>