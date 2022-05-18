<template>
 <div class="container-fluid pt-3">
    <h1 class="text-center py-5">New Courses</h1>

    <div class="row container-cards">
        <div class="col-4 pb-4" v-for="card in cards" :key="card">
          <div class="card w-100" style="width: 15rem">
            <img :src="require('../assets/img/' + card.image)" alt="" />
            <div class="card-body text-center">
              <h5>{{ card.title }}</h5>
              <p>{{card.genre}}</p>
              <div class="card-footer">
                 <span><i class="fa-solid fa-signal"></i>{{card.level}}</span>
                 <span><i class="fa-solid fa-list"></i>{{card.lectures}}</span>
                 <span><i class="fa-regular fa-clock"></i>{{card.durations}}</span>
              </div>
            </div>
          </div>
        </div>
    </div>
   <div class="text-center pt-2 pb-5">
       <button class="btn btn-success load text-center" type="button" id="button-addon2">Load More</button> 
   </div>
 </div>
</template>

<script>
export default {
  name: "CardComponent",
  data() {
    return {
      cards: [
        {
          title: "How to be a DJ? Make Electronic Music",
          image: "Electronic.jpeg",
          genre: "Electronic",
          level: "Advanced",
          lectures: "8 Lectures",
          durations: "6 hours",
        },
        {
          title: "Nvidia and U34 Technologies Practice",
          image: "Nvidia.png",
          genre: "Nvidia",
          level: "Advanced",
          lectures: "8 Lectures",
          durations: "6 hours",
        },
        {
          title: "Fashion Photographiy from professional",
          image: "Fashion.jpeg",
          genre: "Fashion",
          level: "Advanced",
          lectures: "6 Lectures",
          durations: "6 hours",
        },
        {
          title: "Design Instruments for Communication",
          image: "communication.jpeg",
          genre: "Communication",
          level: "Intermediate",
          lectures: "6 Lectures",
          durations: "6 hours",
        },
        {
          title: "Make your Concept Right and Beautiful",
          image: "Art.jpg",
          genre: "Art",
          level: "Intermediate",
          lectures: "6 Lectures",
          durations: "6 hours",
        },
        {
          title: "Road Bike Manual or How to be a Champion.",
          image: "Bicycling.jpeg",
          genre: "Bicycling",
          level: "Beginner",
          lectures: "6 Lectures",
          durations: "6 hours",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
.container-fluid {
  background-color: #edf2f5;

  .container-cards {
    width: 75%;
    display: flex;
    margin: 0 auto;
    position: relative;

    p{
        color: lightgray;
        font-size: 0.75rem;
    }
    .card-footer{
        width: 95%;
        margin: 0 auto;
        background-color:$white;
        display: flex;
        justify-content: space-between;
        span{
            font-size: 0.65rem;
            color: $capeCod;
           i{
              padding-right: 5px;
              color: $butterCup;  
            }
        }
    }
  }
}
.load{
    text-transform: uppercase;
    background-color: $butterCup !important;
    border-color: $butterCup !important;
    border-radius: 52px !important;
    font-size: 0.75rem !important;
    font-weight: bold !important;
}

</style>