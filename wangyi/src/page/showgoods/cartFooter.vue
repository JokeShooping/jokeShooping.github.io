<template>
  <div class="footer">
    <div class="inner">
      <button class="w-button w-button-xxl w-button-noRadius btn btn-icon w-button-ghostWhite">
        <i class="u-icon u-icon-detail-kefu"></i>
      </button>
      <button class="w-button w-button-xxl w-button-noRadius btn btn-text w-button-ghostWhite" @click="toSelect">立即购买</button>
      <button class="w-button w-button-xxl w-button-noRadius btn btn-text" @click="toSelect">加入购物车</button>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    toSelect () {
      // 在商品详情页面
      let type = this.$route.path.split('/')[2]
      let id = this.$route.path.split('/')[4]
      if (this.$route.path.indexOf('select') === -1) {
        this.$router.push({name: 'GoodsSelect', params: {type: type, id: id}})
      } else {
        console.log(type, id)
      }
    }
  }
}
</script>
<style scoped>
.footer{
  position: fixed;
  bottom: 0;
  left: 0;
  z-index: 10;
}
.inner{
  display: flex;
}
.inner .btn.btn-icon {
    flex: 0 0 7rem
} .inner .w-button-ghostWhite {
    border-right: 0;
}.inner .btn {
    align-items: center;
    justify-content: center;
    height: 3rem;
}
.u-icon-detail-kefu {
    background-image: url(http://yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/icon-normal/detail-kefu-aaf8414a44.png);
    width: 5rem;
    height: 1.5rem;
    display: inline-block;
    vertical-align: middle;
    background-repeat: no-repeat;
    background-size: 100% 100%;
}
.inner .btn.btn-text {
    -webkit-box-flex: 1;
    -webkit-flex-grow: 1;
    -moz-flex-grow: 1;
    -ms-flex-positive: 1;
    flex-grow: 1;
} .inner .w-button-ghostWhite {
    border-right: 0;
} 
.w-button, .w-button:focus, .w-button:visited {
    display: inline-block;
    vertical-align: middle;
    width: 8.6rem;
    text-align: center;
    line-height: 2rem;
    font-size: 1rem;
    color: #fff;
    border: 1px solid #b4282d;
    background-color: #b4282d;
    overflow: hidden;
}
.w-button-xxl, .w-button-xxl:focus, .w-button-xxl:visited {
    line-height: 2rem;
}
.inner .btn.btn-text {
    -webkit-box-flex: 1;
    -webkit-flex-grow: 1;
    -moz-flex-grow: 1;
    -ms-flex-positive: 1;
    flex-grow: 1;
}
 .inner .btn {
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    -moz-align-items: center;
    -ms-grid-row-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    -moz-justify-content: center;
    justify-content: center;
    height: 4rem;
}
.w-button-ghostWhite, .w-button-ghostWhite:focus, .w-button-ghostWhite:visited {
    border-color: #c7c7c7;
    color: #333;
    background-color: #fff;
}

</style>
