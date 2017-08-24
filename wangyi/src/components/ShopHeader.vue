<template>
  <div class="shopcart">
      <div class="m-cartHd" >
        <span class="logo" >购物车</span>
        <span class="right" >编辑</span>
    </div>
        <!--promise-->
      <deal-promise></deal-promise>

  </div>
</template>
<script>
import { mapGetters } from 'vuex'
import dealPromise from '@/components/DealPromise'
export default {
  components: {
    dealPromise
  },
  computed: mapGetters(['localUserInfo'])
}
</script>
<style scoped>
.m-cartHd {
    height: 3rem;
    padding: 0 .4rem;
    line-height: 3rem;
    text-align: center;
    background-color: #fff;
    position: relative;
    border-bottom: 1px solid #d9d9d9;
    margin-bottom: .6rem;
}
.logo {
    display: inline-block;
    font-size: 1.2rem;
}
.m-cartHd .right {
    position: absolute;
    top: 0;
    right: .4rem;
    font-size: 1.2rem;
}
.shopcart-promise{
  background-color: #f4f4f4;
}
.shopcart-promise .u-icon-servicePolicy-index {
  display: inline-block;
    vertical-align: middle;
    background-repeat: no-repeat;
    width: 1rem;
    height: 1rem;
}
</style>
