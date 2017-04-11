<template>
  <div id="app">
  <!-- v-show="headerShow" -->
    <NavView v-show="headerShow"  ></NavView>
    <!-- <HomeView></HomeView> -->
    <router-view></router-view>
    <FooterView></FooterView>
  </div>
</template>

<script>
import NavView from './components/Nav.vue'
import HomeView from './components/Home.vue'
import FooterView from './components/Footer.vue'
// 引入vuex 的mapGetters和mapActions
import {mapGetters,mapActions} from 'vuex'

  export default{
    computed:mapGetters([
      'headerShow','footerShow'
    ]),
    watch: {
      $route(to, from) {
        // 对路由变化作出响应...
        console.log(to. path);
        if(to. path=='/user-info'||to. path=='/article'||to. path=='/login'||to. path=='/edit'){
          this.$store.dispatch('hideHeader');
        }else{
          this.$store.dispatch('showHeader');
        }
      }
    },
    components:{
      NavView,
      FooterView
    }
    
  }
</script>

<style>
 
</style>
