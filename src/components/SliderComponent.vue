<template>
  <div>
      <div class="container-slider">
         <ul class="row text-center">
             <li class="col-3">
                 <div class="i">
                     <i class="fa-solid fa-user-group"></i>
                 </div>
                 <h4 class='d-inline-block px-2'>3195</h4>
                 <p class="">Online Learner</p>
             </li>
             <li class="col-3">
                 <div class="i">
                     <i class="fa-solid fa-film"></i>
                 </div>
                 <h4 class='d-inline-block px-2'>23</h4>
                 <p class="">Video Courses</p>
             </li>
             <li class="col-3">
                 <div class="i">
                     <i class="fa-solid fa-image"></i>
                 </div>
                 <h4 class='d-inline-block px-2'>437</h4>
                 <p class="photo">Sliders and Images</p>
             </li>
             <li class="col-3">
                 <div class="i">
                     <i class="fa-solid fa-thumbs-up"></i>
                 </div>
                 <h4 class='d-inline-block px-2'>1440</h4>
                 <p class="">Excellent Reviews</p>
             </li>
         </ul>
      </div>
  </div>
</template>

<script>
export default {
name:'SliderComponent'
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars.scss";
div{
    background-image: url(../assets/img/slider.jpg);

    .container-slider{
        width: 75%;
        margin: 0 auto;
        padding: 100px 0px;

     li{
         list-style: none;
        
        .i{
            display: inline-flex;
            margin-left: -25px;
            color: white;
            font-size: 2.5rem;
        }

        h4{
            vertical-align: text-bottom;
            color: $butterCup;
        }
        .photo{
            font-size: 0.75rem;
            line-height: 0;
            text-align: end;
            padding-right: 13px;
            color: $white;
        }
        p{
            font-size: 0.75rem;
            line-height: 0;
            text-align: end;
            padding-right: 32px;
            color: $white;
        }

     }
        
    }
}
</style>