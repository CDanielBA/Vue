<script setup  >
import { ref } from 'vue';
import  Header  from "./components/Header.vue";
import Card from "./components/Card.vue"
import CardElipse from "./components/CardElipse.vue"
import Gallerys from "./components/Gallerys.vue";

const title1 = ref("");
const title2 = ref("");
const title3 = ref("");
const subtitle1 = ref("");
const subtitle2 = ref("");
const subtitle3 = ref("");
const category1 = ref("");
const category2= ref("");
const category3 = ref("");
const graphic1 = ref("");
const graphic2= ref("");
const graphic3 = ref("");

title1.value = "456K Pcs";
title2.value = "451,509";
title3.value = "$456,623";
subtitle1.value = "Ticket Sold";
subtitle2.value = "Sales";
subtitle3.value = "Income";
category1.value = "Ticket Sold";
category2.value = "Sales";
category3.value = "Income";
graphic1.value = "/src/assets/charts/progressbar.png";
graphic2.value = "/src/assets/charts/line.png";
graphic3.value = "/src/assets/charts/interseccion.png";

</script>

<template>
  <header>
    <Header/>
  </header>

  <main>
    <div class="navbar">
      <a class="link" href="#">Dashboard /</a>
    </div >
    <div class="charts">
      <div class="chart-big">
          <p class="big  rel item1">Best Selling</p>
          <div class="select-time rel item2">
            <p class="gray">this week</p>
            <img src="/src/assets/header/arrow.png" alt="">
        </div>
        <div class="day">
          <p>tuesday</p>
          <p>215,523 pcs</p>
        </div>
        <img src="/src/assets/charts/pieCharts.png" alt="">
        <div class="chart-bar">
          <img src="/src/assets/charts/barChart.png" alt="">
          <img src="/src/assets/charts/x-info.png" alt="">
        </div>
      </div>
      <!-- mobile -->
      <div class="chart-big-mobile">
      <div class="text-top">
        <p class="big  rel item1">Best Selling</p>
        <div class="select-time rel item2">
          <p class="gray">this week</p>
          <img src="/src/assets/header/arrow.png" alt="">
        </div>
        </div>
        <div class="day">
          <p>tuesday</p>
          <p>215,523 pcs</p>
        </div>
        <img class="abs chart-main" src="/src/assets/charts/pieChartsMobile.png" alt="">
      </div>
      <!-- fin mobile -->
      <div class="cont-cards">
        <Card :title="title1" :subtitle="subtitle1" :category="category1" :graphic="graphic1"/>
        <Card :title="title2" :subtitle="subtitle2" :category="category2"  :graphic="graphic2"/>
        <Card :title="title3" :subtitle="subtitle3" :category="category3"  :graphic="graphic3"/>
        <CardElipse/>
      </div >
    </div >
    <div class="gallery">
      <div class="chart-bluesky rel">
        <div>
          <p class="big">Sales Comparison</p>
          <p class="big subtitle">Than last day</p>
        </div>

        <h2 class="percentage">94%</h2>
        <img class="bars abs" src="/src/assets/charts/bars.png" alt="">
        <img class="info abs" src="/src/assets/charts/x-info2.png" alt="">
      </div>
      <Gallerys/>
    </div>
  </main>
</template>

<style scoped>
header {
  display: grid;
  grid-template-columns: 15% 50% 20% 15% ;
  width: 100%;
  margin:30px auto ;
}
.navbar{
  display: flex;
  width: 100%;
  height: 63px;
  background-color: #2f363d;
  align-items: center;
  grid-column-start: 1;
  grid-column-end: 3;
}
.link{
  color:#13B497 ;
  margin-left: 50px;
  text-decoration: none;
}
.item1{
  left: -80px;
}
.item2{
  right: -80px;
}
main{
  display: grid;
  grid-template-columns: 50% 50%;
  width: 100%;
  height: 100vh;
  grid-template-rows: 5% 95%;
}
.select-time{
  display: flex;
  align-items: center;
  gap: 1rem;
}
.select-time img{
  margin: auto;
}
.percentage{
  font-size: 40px;
}
.chart-big{
  padding: 45px;
  background: url("/src/assets/charts/contchartBig.png");
  width: 100%;
  max-width:  936px ;
  max-height: 606px;
  display: grid;
  justify-items: center;
  grid-template-columns: 50% 50%;
}
.chart-big-mobile{
  display: none;
}
.bars{
  width: 800px;
  height: 250px;
  top: 17%;
}
.info{
  top: 80%;
}

.day{
  background-color: #20262d;
  width: 807px;
  height: 61px;
  border-radius: 1rem;
  grid-column-start: 1;
  grid-column-end: 3;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.chart-bar{
  display: flex;
  flex-direction: column;
  margin-top: 60px;
}
.chart-bluesky{
  background: url("/src/assets/charts/background2.png");
  width:936px ;
  height: 439px;
  display: flex;
  justify-content: space-around;
  padding-top: 40px;
  display: block;
  padding-left: 70px;
}
.cont-cards{
  display: grid;
  grid-template-columns: repeat(2,1fr);
}

@media (max-width: 2800px) {
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
  }
}
@media (max-width: 1000px) {
 header{
  grid-template-columns: 35% 35% 30%;
 }
  .cont-cards {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .chart-bluesky {
    display: none;
  }
  .chart-big{
    display: none;
  }
  @media(max-width:620px){
    header{
      display: flex;
    }
    .chart-big-mobile{
      margin: auto;
      display: block;
      width: 350.61px;
      height: 371.69px;
      left: calc(50% - 350.61px/2 + 0px);
      top: 0px;
      background: #272E35;
      box-shadow: 0px 5.89787px 11.3042px rgba(62, 73, 84, 0.04);
      border-radius: 15px;
    }
    .item1{
      left: 20px;
    }
    .day{
      margin: auto;
      width: 90%;
      height: 35px;
      border-radius: 10px;
    }
    .text-top{
      display: flex;
    }
    .chart-main{
      top: 16%;
      left: 0%;
      right: 0%;
      margin: auto;
    }
}
}
</style>
