<template>
     <div class="cell">
     <img src="http://yanxuan.nosdn.127.net/f1dbf1d9967c478ee6def81ed40734a2.png" alt="">
     <div class="right">
       <div class="tagWraper" >
         <p class="status anniversary" >爆品</p>
           </div>
           <p class="hotname" >多功能人体工学转椅</p>
           <p class="desc" >预计5月26日开始发货</p>
           <p class="hotprice" >
             <span >¥</span>
             <span >1399</span>
            </p>
    </div>
    </div>
</template>
<script>
export default {
}
</script>
<style scoped>
.cell{
  border-top: 1px solid #d9d9d9;
  display: flex;
  align-items: center;
  background-color: #fff;
  display: -webkit-flex;
  display: -moz-flex;
  display: -ms-flex;
  display: -o-flex;
}
img{
  width: 7rem;
  height: 8rem;
}
.right{
  text-align: left;
}
 .tagWraper {
    z-index: 1;
    margin-bottom: .4rem;
    overflow: hidden;
}
.right .hotname {
    width: 5rem;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
    font-size: 1.2rem;
    line-height: 1.3rem;
    color: #333;
}
.right .desc {
    font-size: 1rem;
    line-height: 3rem;
    color: #999;
}
.right .hotprice {
    font-size: 0.9rem;
    line-height: 1rem;
    color: #b4282d;
}
</style>
