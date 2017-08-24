<template>
  <div class="header-container">
    <div class="line">
      <router-link to="/" class="logo"></router-link>
      <router-link to="/" class="m-topSearchIpt ipt">
        <i class="icon"></i>
        <span class="placeholder">
          <span>商品搜索, 共</span>
          <span>5116</span>
          <span>款好物</span>
        </span>
      </router-link>
    </div>
    <v-indexTabs :tabs="tabs"></v-indexTabs>
  </div>
</template>

<script>
  import IndexTabs from '@/components/Tabs'
  export default {
    name:'index',
    data(){
      return {

      }
    },
    computed:{
      tabs(){
        return this.$store.getters.headertabList
      }
    }
  }
</script>

<style scoped>
  .header-container{
    background-color: #fff;
    width: 100%;
    height:3rem;
    position: fixed;
  }
  .line{
    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-flex-flow: row nowrap;
    -moz-flex-flow: row nowrap;
    -ms-flex-flow: row nowrap;
    flex-flow: row nowrap;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    -moz-align-items: center;
    align-items: center;
    padding: .3rem .5rem;
  }
  .line .logo{
   width: 6.5rem;
    height: 1.6rem;
    background-image: url("//yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/icon-normal/indexLogo-11d65342f9.png");
    display: inline-block;
    margin-right: 2rem;
    background-size: cover;
    background-position: center;
    /*padding: 0 0 0 0.3rem;*/
  }
  .line>.ipt {
    -webkit-box-flex: 1;
    -webkit-flex-grow: 1;
    -moz-flex-grow: 1;
    -ms-flex-positive: 1;
    flex-grow: 1;
}
.m-topSearchIpt {
    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-flex-flow: row nowrap;
    -moz-flex-flow: row nowrap;
    -ms-flex-flow: row nowrap;
    flex-flow: row nowrap;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    -moz-align-items: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    -moz-justify-content: center;
    justify-content: center;
    height: 2rem;
    font-size: .7rem;
    background-color: #ededed;
    border-radius: .2rem;
    width: 4rem;
}
  .m-topSearchIpt .icon{
    vertical-align: middle;
    background-image: url("http://yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/icon-normal/search2-2fb94833aa.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    margin-right: 0.1rem;
  }
  .m-topSearchIpt .icon{
    display: inline-block;
    width: 1rem;
    height: 1rem;
    margin-left:-3rem;
  }
  .m-topSearchIpt .placeholder {
    color: #666;
    text-decoration: none;
    margin-left: 1rem;
}
</style>