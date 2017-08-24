<template>
  <div class="service-wraper dt-section">
        <div>
          <div class="m-serviceEntry">
            <div class="left">服务</div>
            <div class="right">
              <div class="right-item-wraper">
                <div class="right-item">30天无忧退货</div>
                <div class="right-item">48小时快速退款</div>
              </div>
              <div class="right-item-wraper">
                <div class="right-item">满88元免邮费</div>
                <div class="right-item">网易自营品牌</div>
              </div>
            </div>
            <i class="icon u-icon u-address-right"></i>
          </div>
        </div>
      </div>
</template>
<script>

</script>
<style scoped>
  /*服务*/
  
  .service-wraper {
    padding: .5rem 0;
    background-color: #fff;
  }
  
  .dt-section {
    background: #fff;
    border-bottom: .4rem solid #f4f4f4;
  }
  
  .m-serviceEntry {
    padding-left: .3rem;
    font-size: 0.7rem;
    min-height: 1.6rem;
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
    position: relative;
  }
  
  .m-serviceEntry .left {
    -webkit-align-self: flex-start;
    -moz-align-self: flex-start;
    -ms-flex-item-align: start;
    align-self: flex-start;
    line-height: 1.3rem;
    color: #333;
    font-size: 0.8rem;
    margin-right: .3rem;
  }
  
  .m-serviceEntry .right {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -moz-box-flex: 1;
    -moz-flex: 1;
    -ms-flex: 1;
    flex: 1;
  }
  
  .m-serviceEntry .right .right-item {
    position: relative;
    padding-left: .3rem;
    margin-right: .4rem;
    float: left;
    /*line-height: 1.3rem;*/
    margin-bottom: .4rem;
    color: #7f7f7f;
  }
  
  .m-serviceEntry .right .right-item:after {
    content: "";
    position: absolute;
    width: 0.5rem;
    height: 0.5rem;
    background: #b4282d;
    border-radius: 100%;
    left: -0.2rem;
    top: .3rem;
  }
  
  .m-serviceEntry .u-address-right {
    margin-right: .5rem;
  }
    .u-icon {
    display: inline-block;
    background-size: 100% 100%;
    background-repeat: no-repeat;
    vertical-align: middle;
    width: 0.6rem;
    height: 0.8rem;
  }
  .u-address-right {
    background: url("http://yanxuan.nosdn.127.net/hxm/yanxuan-wap/p/20161201/style/img/icon-normal/address-right-596d39df1e.png") no-repeat;
    background-size: 100% 100%;
}
</style>
