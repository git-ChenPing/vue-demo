<template>
  <div class="main">
    <div class="leftPage">
      <left-page></left-page>
    </div>
    <div class="rightPage">
      <right-page></right-page>
    </div>
  </div>
</template>

<script>
import LeftPage from './LeftPage';
import RightPage from './RightPage';
export default {
  name: 'HelloWorld',
  components:{LeftPage,RightPage},
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main{
  display:flex;
  background-color: rgb(251,251,251);
}
.leftPage{
    flex: 10;
    padding: 0px 70px;
    margin-top: 40px;
}
.rightPage{
    width:300px;
    height: 100vh;
    background-color:#fff;
    border-top-left-radius: 40px;
    border-bottom-left-radius: 40px;
    padding:0 25px;
    box-sizing: border-box;
}
</style>
