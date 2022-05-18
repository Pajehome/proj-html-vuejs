<template>
  <div class="container p-4 justify-content-around d-flex align-items-center">
      
           <img class='w-25' src="../assets/img/master-study.png" alt="">
      
      <ul class='d-inline-flex gap-3 list-unstyled siz'>
          <li  v-for="item in headerLi" :key="item">
             {{item.nav}}
          </li>
          <div class="new">
            new
          </div>
      </ul>

      <div class='d-flex gap-2'>
        <i class="fa-brands fa-linkedin"></i>
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-facebook"></i>
        <i class="fa-brands fa-twitter"></i>
      </div>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: {
    headerLi: Array,
  },
};
</script>

<style  lang='scss'>
@import "../assets/styles/vars.scss";
.siz{
    font-size: 12px;
    padding-top:15px;
    position: relative;

    .new{
       text-transform: uppercase;
       font-size: 8px;
       position: absolute;
       top: 23%;
       right: 32%;
       background-color: red;
       color: $white;
       padding: 0px 2px;
       font-weight: bold;
       border-radius:2px;
    }
  }
    
</style>