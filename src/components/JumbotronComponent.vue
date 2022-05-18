<template>
  <div class="jumbotron position-relative">
   <div class="human-revolution">
       <h1>Start your Human <h1 class="revolution">Revolution </h1> Today</h1>
       <p>A wonderful serenity has taken possession of my entire soul, like these sweet mornings of springs which i enjoy with my whole heart</p>
   </div>

   <div class="sale row">
      <div class="col-6 position-relative">
          <h5 class="text-white">Limited Sale: <h5 class="d-inline-block text-dark"> All courses with 55% off</h5></h5>

          <div class="input-group mb-3 mt-3">
             <input type="text" class="form-control" placeholder="Enter email" aria-label="Recipient's username" aria-describedby="button-addon2">
             <button class="btn btn-success border-rad" type="button" id="button-addon2">Subscribe</button>
          </div>
      </div>
      <div class="col-6">
        <counter-component/>
      </div>
   </div>
  </div>
</template>

<script>
import CounterComponent from './CounterComponent.vue'
export default {
  components: { CounterComponent },
name: 'JumbotronComponent'
}
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
.jumbotron{
    background-image: url(../assets/img/slide-1.jpg);
    height: 80vh;
    background-size:cover;

    .human-revolution{
     width:35%;
     transform: translate(142%, 70%);

        .revolution{
            color: $butterCup;
            display: inline;
        }
    }

    .sale{
        padding: 25px;
        width:75%;
        height: 150px;
        margin: 0 auto;
        transform: translate(0, 210%);
        background-color: $butterCup;
        border-radius: 3px;

        .form-control {
            display: block;
            min-height: calc(1em + .5rem + 2px);
            padding: .35rem .5rem;
            font-size: .75rem;
            font-weight: 400;
            line-height: 1.5;
            color: #495057;
            background-color: #fff;
            background-clip: padding-box;
            border: 1px solid #ced4da;
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
            border-radius: 52px !important;
            transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;


               .form-control:focus {
                    color: #495057;
                    background-color: #fff;
                    border-color: #f9a826;
                    outline: 0;
                    box-shadow: none;
                }
            }
        .border-rad{
           @include button-rad;  
        }
  
    }
}
</style>