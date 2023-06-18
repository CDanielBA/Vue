<script>
export default {
  name: 'Card',
  props: {
    title: String,
    subtitle:String,
    category:String,
    graphic:String,
  },
  data() {
    return {
      internalTitle: '',
      internalsubTitle: '',
      internalgraphic: '',
      internalcategory: ''
    };
  },
  created() {
    this.internalTitle = this.title;
    this.internalsubTitle = this.subtitle;
    this.internalcategory = this.category;
    this.internalgraphic = this.graphic;
  }
};
</script>

<template>
  <div class="cards">
    <div class="texts">
      <div>
        <p class="big">{{ internalTitle }}</p>
        <p class="gray sm">{{ internalsubTitle }}</p>
      </div>
      <div class="info-category">
        <p>{{ internalcategory }}</p>
        <img src="../assets/header/arrow.png" alt="">
      </div>
    </div>
    <div class="graphic">
      <img class="img-graphic rel" :src="internalgraphic" alt="">
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
.img-graphic{
  width: 420px;
  top: 20%;
}
</style>