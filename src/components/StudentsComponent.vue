<template>
  <div class="container-students">
     <h1>What Students Say</h1>
     <div class="row justify-content-between g-0 align-items-center py-4">
       <div class="col-4 w-25 h-100">
         <i class="fa-solid fa-arrow-left-long"></i>
       </div>
       <div class="col-4 d-flex gap-2 justify-content-center align-items-center">
         <img  src="../assets/img/1-100x100.jpg" alt="">
         <img  class="active" src="../assets/img/2-100x100.jpg" alt="">
         <img src="../assets/img/4-100x100.jpg" alt="">
       </div>
       <div class="col-4 w-25">
         <i class="fa-solid fa-arrow-right-long"></i>
       </div>
     </div>
    
    <h4>Paints of the Future</h4>
    <span v-for="num in 5" :key='num'>
       <i class="fa-solid fa-star butter-cup"></i>
    </span>
    <div class="review d-flex justify-content-center pt-4">
      <p class="w-75"> The response to your MasterStudy has been really overwhelming! Those who participated in the workshop are spreading the word here on campus and the “buzz” is on. The VP of Instruction wants you to come back! Her goal is to have more faculty trained. She also wants to attend a workshop herself. Our President told me Masterstudy needs to be the cornerstone of our success program.”</p>
    </div>
  </div>
</template>

<script>
export default {
name: 'StudentsComponent'
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars.scss";
.container-students{
  width: 75%;
  margin: 0 auto;
  text-align: center;
  padding: 50px 0px;
  
  img{
    border-radius: 50%;
    width: 25%;
    height: 25%;
  }
  .active{
      width: 8vw;
  }
  .butter-cup{
    color: $butterCup;
  }
}

</style>