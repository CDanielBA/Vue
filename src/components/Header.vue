<script>
export default {
  name: 'Header',
}
// defineProps({
//   msg: {
//     type: String,
//     required: true
//   }
// })
</script>

<template>
    <menu>
      <img class="burger" src="../assets/header/hamburgermenu_120234.png" alt="">
      <img src="../assets/header/logo.png" alt="">
    </menu>
    <div class="search">
      <input type="text" class="input-search" placeholder="search here">
      <div class="btn-noti-skyblue">
        <img src="../assets/icons/setting.png" alt="">
      </div>
    </div>
    <div class="notis">
      <div class="btn-noti">
        <img src="../assets/icons/msg.png" alt="">
      </div>
      <div class="btn-noti">
        <img src="../assets/icons/noti.png" alt="">
      </div>
      <div class="btn-noti">
        <img src="../assets/icons/sorprese.png" alt="">
      </div>
    </div>
    <div class="user">
      <img src="../assets/header/placeholder.png" alt="">
      <div class="info-user">
        <p>Daniel</p>
        <img class="arrow" src="../assets/header/arrow.png" alt="">
      </div>
    </div>
</template>


<style>
.burger{
  filter: brightness(0) invert(1);
}

menu{
  display: flex;
  align-items: center;
}
.notis, .search{
  display: flex;
  gap: 1rem;
  align-items: center;
}
.info-user{
  display: flex;
  justify-content: space-around;
}
.info-user p{
  display: flex;
  justify-content: space-around;
  width: 80%;
  margin: auto;
}
.user{
  background: url("../assets/header/background.png");
  display: grid;
  position: relative;
  width:182px ;
  height:58px ;
  grid-template-columns: 30% 70%;
  align-items: center;
}
.arrow{
  margin: auto;
}
.input-search{
  width: 500px;
  background-color: #1c2126;
  border: none;
  border-radius: 1rem;
  height: 50px;
  display: block;

}
.btn-noti,.btn-noti-skyblue{
  background-color: #2f363d;
  width: 56px;
  height: 56px;
  border-radius: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.btn-noti-skyblue{
  background-color: #13b497;
  display: flex;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media(max-width:1000px){
.input-search, .btn-noti-skyblue{
  display: none;
}
.search{
    display: none;
  }
}
@media(max-width:620px){
  .notis .btn-noti:nth-child(2){
    display: none;
  }
  .info-user p{
    display: none;
  }
}
</style>