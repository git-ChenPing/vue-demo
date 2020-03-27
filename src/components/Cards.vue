<template>
  <div>
      <div class="cardTop">
          <div style="font-weight:bold">Cards</div>
          <div style="color:gray;font-size:12px">view all cards</div>
      </div>
      <div class="cards">
          <div v-for="item in list" :key="item.id" :class="item.styles"></div>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            list: [
                {
                    styles: 'black',
                    id:1
                },
                {
                    styles: 'green',
                    id:2
                },
                {
                    styles: 'orange',
                    id:3
                },
                {
                    styles: 'prink',
                    id:4
                }
            ]
        }
    }
}
</script>

<style scoped>
.cardTop{
    display: flex;
    justify-content: space-between;
    margin: 40px 0 20px 0;
}
.black{
    background-color:black;
    width: 270px;
    height:140px;
    border-radius: 20px;
    margin-top:20px;
}
.green{
    background-color: green;
    width: 270px;
    height:140px;
    border-radius: 20px;
    margin: 0 20px;
    margin-top:20px;
}
.orange{
    background-color: orange;
    width: 270px;
    height:140px;
    border-radius: 20px;
    margin-top:20px;
    margin-right: 20px;
}
.cards{
    display:flex;
    flex-wrap: wrap;
}
.prink{
    background-color: pink;
    width: 270px;
    height:140px;
    border-radius: 20px;
    margin-top:20px;
}
</style>