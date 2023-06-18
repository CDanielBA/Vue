<script>
export default {
  name: 'Card'
}
</script>

<template>
  <div class="cards">
    <div class="texts">
      <div>
        <img class="elipse rel" src="../assets/charts/pieChart.png" alt="">
      </div>
      <div class="info-category">
        <p>This Week</p>
        <img src="../assets/header/arrow.png" alt="">
      </div>
    </div>
    <div class="graphic">
      <img class=" legend rel" src="../assets/charts/legend.png" alt="">
    </div>
  </div>
</template>

<style>
.cards {
  display: grid;
  background: url("../assets/charts/backgroundCard.png");
  width: 481px;
  height: 239px;
  grid-template-columns: 50% 50%;
  grid-template-rows: 20% 80%;
  padding: 25px ;
}
.texts{
  display: flex;
  justify-content: space-around;
  grid-column-start: 1;
  grid-column-end: 3;
}
.info-category{
  display: flex;
  align-items: center;
  gap: 1rem;
}
.info-category img{
  margin: auto;
}
.legend{
  top: 30%;
  right: -80%;
}
.elipse{
  left: -25%;
  top: 20%;
}
</style>