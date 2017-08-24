<template>
  <header>
    <div class="inner">
      <div class="list">
        <div class="list-container">
          <div class="tab" :class="{active:item.isActive}" v-for="item in tabs" :key="item.id">
            <router-link to="item.linkTo">
              <span class="txt" @click="activethis(item.id)">{{item.name}}</span>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  export default {
    props:["tabs"],
    data (){
      return {

      }
    },
    methods: {
      activethis(id){
         // 找出当前激活的选项，当前点击的选项
        if(this.$store.path.indexOf("type")>=0){
          this.$store.dispatch("changeTypesabActive",id)
          return false
         }
         if(this.$router.path.indexOf("mylist")>=0){
          this.$store.dispatch("changeTypesabActive",id)
          return false
         }
         console.log(id);
         this.$store.dispatch("changeTypesabActive",id)
      }
    }
  }
</script>

<style scoped>
header {
    height: .8rem;
}

 header.mylist .inner .list {
  display: flex;
  width: 100%;
  justify-content:space-around;
 }
 header{
    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-flex-flow: row nowrap;
    -moz-flex-flow: row nowrap;
    -ms-flex-flow: row nowrap;
    flex-flow: row nowrap;
    background-color:#fff;
    height: 1rem;
    position: relative; 
 }
</style>