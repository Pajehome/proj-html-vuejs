<template>
  <div class="text-center pt-5">
    <h1>Why my Courses?</h1>
    <div class="container-book">
      <div class="row gap-3 justify-content-center ">
        <div
          class="card col-6 py-2 bord-shad"
          style="width: 24rem"
          v-for="item in vantages"
          :key="item">
          <div class="card-body row">
            <div class="col-2">
              <i :class="item.awesome"></i>
            </div>
            <div class="col-10">
              <h5 class="card-title tit">{{ item.learn }}</h5>
              <p class="info">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WhyComponent",
  data() {
    return {
      vantages: [
        {
          learn: "Entrepreneurship",
          awesome: "fa-solid fa-briefcase",
        },
        {
          learn: "Accelerated learning",
          awesome: "fa-solid fa-rocket",
        },
        {
          learn: "Productivity",
          awesome: "fa-solid fa-thumbs-up",
        },
        {
          learn: "Life Coaching",
          awesome: "fa-solid fa-gear",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars.scss";
.container-book {
  width: 75%;
  display: flex;
  margin: 0 auto;
  padding: 30px 0px;

  .info {
    color: lightgray;
    text-align: left;
    width: 100%;
  }
  .tit{
      text-align: left;
      width: 100%;
      color: $shark;
  }

  i{
    font-size: 2rem;
    color: $butterCup;
  }

  .bord-shad{
      border-left: 4px solid $butterCup !important;
      border-radius: 0 !important;
      border: 0px;
      box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  }
  

}
</style>