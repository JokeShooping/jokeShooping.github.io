<template>
  <div class="m-attrCon" >
      <div class="attrList">
        <div class="tt" >商品参数</div>
        <div class="item" v-for="item in attr">
          <div class="left" >{{item.left}}</div>
          <div class="right" >
            <div class="con">{{item.right}}</div>
          </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  props: ['attr']
}
</script>
<style scoped>
/*商品参数*/
.m-attrCon {
    padding: .4rem;
    background-color: #fff;
}
.m-attrCon .attrList .tt {
    padding: .6rem 0 .4rem;
    font-size: 1.2rem;
    line-height: 1;
}
.m-attrCon .attrList .item {
    zoom: 1;
    font-size: 1.2rem;
    line-height: 1rem;
    padding: .3rem .4rem .2rem 0;
    background-image: linear-gradient(to right,#919191 33%,rgba(255,255,255,0) 0);
    background-position: top;
    background-size: 12px 1px;
    background-repeat: repeat-x;
}
.m-attrCon .attrList .item .left {
    float: left;
    width: 12rem;
    position: relative;
    color: #999;
}
.m-attrCon .attrList .item .right {
    margin-left: 3rem;
}
</style>
