<template>
  <div class="LeftPageBottom">
      <div class="left">
          <main-service></main-service>
      </div>
      <div class="right">
          <main-service-right></main-service-right>
      </div>
  </div>
</template>

<script>
import MainService from './MainService';
import MainServiceRight from './MainServiceRight'
export default {
    components:{MainService, MainServiceRight},
    data(){
        return {

        }
    }
}
</script>

<style scoped>
.LeftPageBottom{
    display:flex;
    margin-top:80px;
}
.left{
    width: 250px;
}
.right{
    flex:1;
    height: 50vh;
}
</style>