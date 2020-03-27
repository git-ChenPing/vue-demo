<template>
  <section>
      <div class="navTop">
          <div class="logoImg">
              <img src="@/assets/logo.png" alt="">
          </div>
          <div class="navBar">
              <ul>
                  <li>Dashborad</li>
                  <li>Services</li>
                  <li>History</li>
                  <li>Actions</li>
              </ul>
          </div>
          <div class="searchInput">
              <input type="text" placeholder="search...">
              <img src="@/assets/searchIcon.png" alt="" style="width:24px">
          </div>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
.navTop{
    display: flex;
    justify-content: space-between;
    align-items:center;
}
.logoImg>img{
    width:50px;
    padding-right: 50px;
}
.searchInput{
    border:1px solid rgb(248,248,248);
    border-radius: 40px;
    padding:0 10px;
    background-color: rgb(248,248,248);
    width: 210px;
}
.searchInput>img{
    vertical-align: middle;
}
.searchInput>input{
    border:0;
    outline: 0;
    padding: 5px 0;
    margin-left: 10px;
    height:22px;
    background-color: rgb(248,248,248);
}
.searchInput>input::placeholder{
    color: rgb(207,208,212);
}
.navBar>ul{
    display: flex;
    flex: 1;
    justify-content: space-around;
}
.navBar>ul>li{
    padding-right: 40px;
}
</style>