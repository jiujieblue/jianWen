<template>
<div class="login_content">
    <p class="fhbtn"><a href="javascript:;" @click="goBack()"></a></p>
    <h1></h1>
    <div class="login-box">
    	<p class="lsolid"></p>
        <div class="login">

        	<a href="javascript:;">登录</a><span></span>
        	<a href="javascript:;">注册</a>
        </div>
        <p class="rsolid"></p>
    </div>
    <ul>
        <li class="lifirst">
        	<input type="text" value=""/>
            <span>帐号</span>
        </li>
        <li>
        	<input type="password" value=""/>
            <span>密码</span>
        </li>
    </ul>
    <div class="footbox">
        <router-link to="/home">
        	<input type="button" value="登 录" class="login-btn"/>
        </router-link>
        <a href="javascript:;" class="tishi">忘记密码？</a>
    </div>
</div>
</template>
<style>
	body{ background:#f2f4f5;}
	.login_content{max-width:6.4rem; margin:0 auto;}
	.login_content .fhbtn{ padding-top:0.27rem;}
	.login_content .fhbtn a{ display:block;width:0.23rem;height:0.25rem; background:url(../assets/img/history1.png) no-repeat 0 0; background-size:100%; margin-left:0.3rem;}
	.login_content h1{width:2.18rem;height:1.35rem; background:url(../assets/img/logo.png) no-repeat 0 0; background-size:100%; margin:0 auto; margin-top:1.22rem;}
	.login_content .login{width:2.0rem;height:0.38rem; margin:0 auto; margin-top:0.85rem;}
	.login a{width:0.97rem;height:0.38rem; font-size:0.35rem; line-height:0.38rem; float:left; color:#4c4f50; text-align:center;}
	.login span{ float:left;height:0.38rem; border-left:1px solid #4c4f50;}
	.login_content .login-box{ position:relative;}
	.login_content .login-box .lsolid{width:1.96rem;height:0.18rem; border-bottom:1px solid #4c4f50; position:absolute;top:0;left:0.1rem;}
	.login_content .login-box .rsolid{width:1.96rem;height:0.18rem; border-bottom:1px solid #4c4f50; position:absolute;top:0;right:0.1rem;}
	.login_content ul{width:5.78rem;height:1.92rem; border:1px solid #e5e7e8; background:#fff; margin:0 auto; margin-top:0.68rem;}
	.login_content ul li{height:0.95rem; position:relative;}
	.login_content ul li.lifirst{border-bottom:1px solid #e5e7e8;}
	.login_content ul li input{ padding-left:1.5rem;width:4.54rem;height:100%; font-size:0.4rem;}
	.login_content ul li span{width:1.23rem;height:0.49rem; position:absolute;top:0.26rem;left:0; border-right:1px solid #676868; color:#676868; font-size:0.25rem; line-height:0.49rem; text-align:center;}
	.login_content .footbox{width:4.65rem;height:0.65rem;margin:0 auto; }
	.login_content .login-btn{width:4.65rem;height:0.65rem; background:#f85959; color:#fff; text-align:center; line-height:0.65rem; border-radius:8px; display:block; margin-top:0.62rem; font-size:0.28rem;}
	.login_content .tishi{width:1.4rem; font-size:0.25rem; margin-top:0.28rem; display:block;}
</style>\
<script>
	export default{
		methods:{
			goBack:function(){
			window.history.go(-1);	
		}
		}
	}
</script>