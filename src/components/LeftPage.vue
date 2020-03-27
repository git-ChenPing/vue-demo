<template>
  <div>
      <nav-top></nav-top>
      <cards></cards>
      <left-page-bottom></left-page-bottom>
  </div>
</template>

<script>
import NavTop from './NavTop'
import Cards from './Cards'
import LeftPageBottom from './LeftPageBottom'
export default {
    components:{NavTop, Cards, LeftPageBottom},
    data(){
        return {

        }
    }
}
</script>

<style scoped>

</style>