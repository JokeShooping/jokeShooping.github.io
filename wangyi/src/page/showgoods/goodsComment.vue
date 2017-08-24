<template>
  <!--评价-->
  <div class="m-detailComment">
    <header>
      <h3 class="title">
        <span>评价(</span>
        <span>225</span>
        <span>)</span>
      </h3>
      <div class="comment-checkAll">
        <span>查看全部</span>
        <i class="u-icon u-address-right icon"></i>
      </div>
    </header>
    <div class="g-c">
      <div class="m-comment m-comment-detail">
        <header>
          <div class="left">
            <img class="avatar" :src="comment.first.avatar">
            <span class="name" >{{comment.first.name}}</span>
            <i class="u-icon u-icon-v1"></i>
          </div>
          <div class="right">
            <span class="time">2017-05-25 21:47:49</span>
          </div>
        </header>
        <div class="content">
          <div class="inner" >{{comment.first.content}}</div>
        </div>
        <div class="commentPics">
          <div class="m-commentPics">
            <ul class="list">
              <li class="item-wrap"  v-for="item in comment.first.imgs">
                <div class="item">
                  <img :src="item" style="width: 100%;"></div>
              </li>
            
            </ul>
          </div>
        </div>
        <p class="skus" {{comment[0].hechoose}}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ['comment']
}
</script>
<style scoped>
/*评论*/
.m-detailComment {
  border-bottom: .4rem solid #f4f4f4;
  background-color: #fff;
}
  .m-detailComment>header {
    margin-left: .4rem;
    position: relative;
    border-bottom: 1px solid #d9d9d9;
    padding: .4rem 2.4rem .4rem 0;
}
.m-detailComment>header .title {
    line-height: 1.6rem;
    font-size: 1.2rem;
    color: #333;
}
.m-detailComment>header .comment-checkAll {
    padding-right: .6rem;
    right: .5rem;
    font-size: 1rem;
    color: #333;
    height: .6rem;
    line-height: .6rem;
}
.m-detailComment>header .comment-checkAll, .m-detailComment>header .comment-checkAll .icon {
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 0;
}
.m-detailComment>header .comment-checkAll .icon {
    position: absolute;
    margin: auto;
    top: 0;
    bottom: 0;
}
.u-address-right {
    background: url(http://yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/icon-normal/address-right-596d39df1e.png) no-repeat;
    background-size: 100% 100%;
    width: 1rem;
    height: 1rem;
    right: 0;
}
.u-icon {
    display: inline-block;
    background-size: 100% 100%;
    background-repeat: no-repeat;
    vertical-align: middle;
}
.g-c {
    zoom: 1;
    padding: 0 .4rem;
}
.m-comment-detail {
    padding-bottom: .42667rem;
}
.m-comment header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: .4rem 0 .3rem;
    margin-top: 4px;
}

.m-comment header .left {
    zoom: 1;
    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    -moz-align-items: center;
    align-items: center;
    font-size: 1.2rem;
}
.m-comment header .left .avatar {
    width: 1rem;
    height: 1rem;
    margin-right: .4rem;
    border-radius: 50%;
    overflow: hidden;
}
.m-comment header .left .name {
    margin-right: .4rem;
}
.m-comment .u-icon-v1 {
    background-position: 0 -69.22667rem;
}
.m-comment .u-icon-v1, .u-icon-v2,.m-comment .u-icon-v3, .u-icon-v4 {
    display: inline-block;
    vertical-align: middle;
    background-image: url(http://yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/sprites/membership-sc86699d936-cc4229a2e5.png);
    background-repeat: no-repeat;
    background-size: 2rem 71.22667rem;
    width: .56rem;
    height: .56rem;
}
.icon{
  width: 1rem;
  height: 1rem;
}
.m-comment header .time {
    font-size: 1rem;
    color: #999;
}
.m-comment .content {
    margin-bottom: .6rem;
    padding-right: .4rem;
    margin-top: 0;
}
.m-comment .commentPics {
    margin-bottom: .5rem;
}
.m-commentPics .list {
    overflow: hidden;
}
.m-commentPics .list .item-wrap {
    z-index: 1;
    float: left;
    border: 1px solid #d9d9d9;
    margin-right: .6rem;
    border-radius: 4px;
}
.m-commentPics .list .item, .m-commentPics .list .item-wrap {
    position: relative;
    width: 2rem;
    height: 2rem;
    overflow: hidden;
}
.m-commentPics .list .item, .m-commentPics .list .item-wrap {
    position: relative;
    width: 2rem;
    height: 2rem;
    overflow: hidden;
}
.m-commentPics .list .item img {
    position: absolute;
    left: 50%;
    top: 50%;
    -moz-transform: translate3D(-50%,-50%,0);
    -ms-transform: translate3D(-50%,-50%,0);
    -webkit-transform: translate3D(-50%,-50%,0);
    transform: translate3D(-50%,-50%,0);
    display: block;
}
.m-comment .skus {
    line-height: 1;
    font-size: 1rem;
    color: #999;
}
/*商品参数*/
.m-attrCon {
    padding: .4rem;
    background-color: #fff;
    /*height: 2rem;*/
}
.m-attrCon .attrList .tt {
    padding: .6rem 0 .4rem;
    font-size: 1rem;
    line-height: 1rem;
    height: 4rem;
}
.m-attrCon .attrList .item {
    zoom: 1;
    font-size: 1.2rem;
    line-height: 0.8rem;
    padding: .13333rem .4rem .13333rem 0;
    background-image: -webkit-gradient(linear,left top, right top,color-stop(33%, #919191),color-stop(0, rgba(255,255,255,0)));
    background-image: linear-gradient(to right,#919191 33%,rgba(255,255,255,0) 0);
    background-position: top;
    background-size: 12px 1px;
    background-repeat: repeat-x;
}
.m-attrCon .attrList .item .left {
    float: left;
    width: 2rem;
    position: relative;
    color: #999;
}
.m-attrCon .attrList .item .right {
    margin-left: 3rem;
}
</style>
