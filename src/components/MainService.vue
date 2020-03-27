<template>
  <div>
    <div class="mainService">
        <div style="font-weight:bold;">
          Main service
        </div>
        <div>
          <span>View all</span>
        </div>
    </div>
    <div>
      <ul>
        <li>
          <img src="@/assets/1.png" alt="">
          <p>Transcations</p>
        </li>
        <li>
          <img src="@/assets/2.png" alt="">
          <p>Utlity</p>
        </li>
        <li>
          <img src="@/assets/3.png" alt="">
          <p>Loans</p>
        </li>
        <li>
          <img src="@/assets/4.png" alt="">
          <p>Deposits</p>
        </li>
        <li>
          <img src="@/assets/5.png" alt="">
          <p>Fast transfer</p>
        </li>
        <li>
          <img src="@/assets/6.png" alt="">
          <p>Exchange</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.mainService{
  display: flex;
  justify-content: space-between;
}
.mainService>div>span{
  color: gray;
  font-size: 12px;
}
ul{
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  align-items: center;
  text-align: center;
}
ul>li{
  width: 100px;
  font-size: 12px;
  padding: 20px 0;
  margin-top: 20px;
  background-color:#fff;
  box-shadow: 1px 1px 1px black;
  border-radius: 15px;
  box-shadow: 10px 6px 2px rgb(248,248,248);
}
ul>li>p{
  margin-top: 5px;
}
</style>