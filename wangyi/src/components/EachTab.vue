<template>
  <div>
    <div class="slideWarp">
      <img :src="desc.adpic" alt="" class="advertisement">
    </div>
   <good-grid :data="desc.data"></good-grid>
  </div>
</template>

<script type="text/javascript">
    import goodsGrid from '@/components/GoodsGrid'
    export default{
      props:['desc'],
      data (){
        return {

        }
      },
      components:{
        goodsGrid
      }
    }
</script>

<style type="text/css">
.slideWarp{
  margin-bottom: .3rem;
}
</style>