<template>
<div class="content " >
	<div class="user-header">
        <router-link to="/login">
        	<h2><img src="../assets/img/headimg.png" alt=""/></h2>
            <div class="user-box">
                    <a href="javascript:;">登录</a>
                   <a href="javascript:;">注册</a>
                
            </div>
        </router-link>
        <ul class="clear">
        	<li>
            	<span>0</span>
                <p>关注</p>
            </li>
            <li>
            	<span>0</span>
                <p class="end">粉丝</p>
            </li>
        </ul>
    </div>
    <div class="docList">
    	<ul>
            <li class="gk-text">
            	<i></i>
                <p>公开博文</p>
                <b></b>
                <span>0</span>
            </li>
            <li class="mm-text">
            	<i></i>
                <p>秘密博文</p>
                <b></b>
                <span>0</span>
            </li>
            <li class="cg-text">
            	<i></i>
                <p>草稿箱</p>
                <b></b>
                <span>0</span>
            </li>
            <li class="sc-text">
            	<i></i>
                <p>收藏夹</p>
                <b></b>
                <span>0</span>
            </li>
            <li class="my_cz">
            	<i></i>
                <p>收藏夹</p>
            </li>
        </ul>
    </div>
</div>
</template>
<script>
// import	'../assets/css/mydoc.css'
require('../assets/css/mydoc.css');
</script>
<style>
.pt30{
	padding-top: 30px;
}
</style>