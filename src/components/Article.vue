<template>
	<div class="cont">
		<div class="atnav ">
			<ul>
		    	<li class="l-btn" @click="goBack()"></li>
		    </ul>
		</div>
		<div class="at-content">
			<div class="content-header clear"><h2><img :src="homeArticleData[2].author_face" alt=""/></h2><p>新闻编辑</p></div>
		    <div class="cont">
		    	<h3>{{homeArticleData[1].title}}</h3>
		        <div class="time">
		        	<p>
		        		{{homeArticleData[1].time}}
		        		<span><img src="../assets/img/zan.png" alt=""/></span>
		        	</p>
		        </div>
		        <div class="text-box" v-html="homeArticleData[1].content">
		        </div>
		    </div>
		</div>
		<div class="at-foot-btn">
			<ul>
		    	<li class="say"><a href="javascript:;">
		        	<i></i><span>0</span>
		        </a></li>
		    	<li class="zan"><a href="javascript:;">
		        	<i></i><span>0</span>
		        </a></li>
		    	<li class="xing"><a href="javascript:;">
		        	<i><img src="../assets/img/xing.png" alt=""/></i>
		        </a></li>
		    	<li class="fx"><a href="javascript:;">
		        	<i><img src="../assets/img/fx.png" alt=""/></i>
		        </a></li>
		    </ul>
		</div>
	</div>
</template>
<style>
	.atnav{width:100%; position:fixed;top:0;left:0; background:#fff; border-bottom:1px solid #e8eaec; z-index:99;}
	.atnav ul{width:6.4rem;height:0.45rem; padding-top:0.15rem; margin:0 auto;}
	.atnav ul li{width:0.29rem;height:0.31rem; background:url(../assets/img/history.png) no-repeat 0 0; background-size:0.29rem 0.31rem; margin:0 0 0 0.38rem;}
	
	.at-content{max-width:6.4rem; margin:0 auto; margin-top:0.6rem; background:#f2f4f5; padding-bottom:0.85rem;}
	.at-content .content-header{ padding:0.39rem 0.28rem 0.15rem 0.28rem;}
	.content-header h2{ float:left; margin-right:0.18rem;}
	.content-header h2 img{  	 height: 0.6rem;   }
	.content-header p{ float:left; line-height: 0.6rem;  font-size:0.22rem; color: #666;}
	
	.at-content .cont{ padding:0 0.38rem; color:#494d4d;}
	.cont h3{ font-size:0.4rem; line-height:0.6rem; padding-bottom:0.25rem; border-bottom:1px solid #b1b1b1;}
	.cont .time{height:0.24rem; line-height:0.24rem; margin:0.26rem 0; }
	.time p{ float:left;position:relative;}
	.time span{width:0.33rem;height:0.32rem; position:absolute; top:-0.02rem;right:-0.35rem;}
	.time span img{width:100%;height:100%;}
	
	.cont .text-box{ font-size:0.25rem;}
	.text-box p{ line-height:1.5!important; margin-bottom:0.1rem;}
	.at-foot-btn{width:100%;height:0.8rem; background:#fff; border-top:1px solid #e8eaec; position:fixed; left:0;bottom:0;}
	.at-foot-btn ul{width:6.4rem; margin:0 auto;height:0.52rem; margin-top:0.16rem;}
	.at-foot-btn ul li{ float:left;}
	.at-foot-btn ul li a{width:100%;height:100%; display:block;}
	.at-foot-btn ul .say{width:2.03rem;height:0.52rem; border-right:1px solid #e8eaec;}
	.say i{width:0.36rem;height:0.26rem; background:url(../assets/img/say.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.7rem; margin-top:0.13rem;}
	.say span{height:0.26rem; float:left; line-height:0.26rem; margin-left:0.16rem; margin-top:0.13rem;}
	.at-foot-btn ul .zan{width:1.86rem;height:0.52rem; border-right:1px solid #e8eaec;}
	.zan i{width:0.36rem;height:0.28rem; background:url(../assets/img/zan1.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.54rem; margin-top:0.13rem;}
	.zan span{height:0.26rem; float:left; line-height:0.26rem; margin-left:0.16rem; margin-top:0.13rem;}
	.at-foot-btn ul .xing{width:1.2rem;height:0.52rem; border-right:1px solid #e8eaec;}
	.xing i{width:0.34rem;height:0.24rem; margin:0 auto; display:block; padding-top:0.1rem;}
	.xing i img{width:100%;}
	.at-foot-btn ul .fx{width:1.25rem;height:0.52rem;}
	.fx i{width:0.33rem;height:0.08rem;display:block; margin:0 auto; padding-top:0.15rem;}
	.fx i img{width:100%;}
</style>
<script>
export default{
	data(){
		return{
			homeArticleData:[]
		}
	},
	mounted(){
		//获取数据
		this.getArticleData();
	},
	methods:{
		goBack:function(){
			// alert('11');
			// window.history.go(-1);	
			window.history.go(-1);
		},
		getArticleData(){
			var _this=this;
			this.$http.get('./src/data/article.data').then(function (res) {
				_this.homeArticleData=res.data;
				console.log(res.data);
			}).catch(function(err){
				alert(' 请求数据失败'+err)
			});
		}
	}
}
</script>