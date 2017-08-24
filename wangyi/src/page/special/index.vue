<template>
  <div class="special">
    <div class="container">
      <no-loop-swiper :Items="Items" class="special-no-loop"></no-loop-swiper>
      <each-suggest :suggests="suggests"></each-suggest>
    </div>
    <v-footer class="footer"></v-footer>
  </div>
</template>

<script>
import data from '@/fetch/api'
import Footer from '@/components/Footer'
import noloopswiper from '@/components/NoLoopSwiper'
import eachSuggest from '@/components/EachSuggest'
export default {
  name: 'index',
  data () {
    return {
      Items: [
        {id: 0, src: 'https://yanxuan.nosdn.127.net/1de4da49367dd7c01af1f7a2b23b0237.jpg'},
        {id: 1, src: 'https://yanxuan.nosdn.127.net/14939888168151095.png'},
        {id: 2, src: 'https://yanxuan.nosdn.127.net/dc1b671ad54e16339f1b26cfeec6a1ea.jpg'},
        {id: 3, src: 'https://yanxuan.nosdn.127.net/d943675462a06f817d33062d4eb059f5.jpg'},
        {id: 4, src: 'http://www.51pptmoban.com/d/file/2015/11/27/2123f7686d354b4d1b67b99a7f657747.jpg'},
        {id: 5, src: 'http://imgs13.iaweg.com/pic/HTTP3d3dy5mZWl6bC5jb20vdXBsb2FkMjAwNy8yMDEwXzA1LzEwMDUyODAwNTA4NjYyMS5qcGclog.jpg'}
      ],
      suggests: []
    }
  },
  created () {
    this.$Loading.config({
      color: '#b4282d',
      failedColor: '#f0ad4e',
      height: 3
    })
    this.$Loading.start()
    this.$store.dispatch('changeActive', 1)
    data.getTypeDesc('specials').then(res => {
      this.suggests = res
      console.log('res', res)
    })
  },
  mounted () {
    this.$Loading.finish()
  },
  computed: {
  },
  components: {
    'v-footer': Footer,
    'no-loop-swiper': noloopswiper,
    eachSuggest
  }
}
</script>

<style scoped>
.container{
    margin-bottom: 1.30667rem;
}
.swiper-container img{
     width: 5rem;
    height: 3rem;
    border-radius: .2rem;
}
.swiper-container .swiper-slide{
  margin-right: 0 !important;
}
.special-no-loop {
  background-color: #fff;
  padding: .26667rem .4rem;
  margin-bottom: .26667rem;
}

</style>
