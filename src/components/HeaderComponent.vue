<template>
  <div class="container p-4 justify-content-around d-flex align-items-center">
    <img class="w-25" src="../assets/img/master-study.png" alt="" />

    <ul class="d-inline-flex gap-3 list-unstyled siz">
      <li v-for="item in headerLi" :key="item">
        <a href="#">{{ item.nav }} &dtrif;</a>
        <ul class="dropdown">
          <li v-for="item in headerLi" :key="item"><a href="#">{{item.nav}}</a></li>
        </ul>
      </li>
      <div class="new">new</div>
    </ul>

    <div class="d-flex gap-2">
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
.siz {
  font-size: 12px;
  padding-top: 15px;
  position: relative;

  .new {
    text-transform: uppercase;
    font-size: 8px;
    position: absolute;
    top: 23%;
    right: 32%;
    background-color: red;
    color: $white;
    padding: 0px 2px;
    font-weight: bold;
    border-radius: 2px;
  }
}

ul li ul {
  visibility: hidden;
  opacity: 0;
  position: absolute !important;
  padding-left: 0;
  display: none;
  background: white;
  z-index: 1;
}

ul li:hover > ul,
ul li ul:hover {
  visibility: visible;
  opacity: 1;
  display: block;
  min-width: 120px;
  text-align: left;
  padding-top: 20px;
  box-shadow: 0px 3px 5px -1px #ccc;
}

ul li ul li {
  clear: both;
  width: 100%;
  text-align: left;
  margin-bottom: 20px;
  border-style: none;
  list-style: none;
}

ul li ul li a:hover {
  padding-left: 10px;
  border-left: 2px solid #3ca0e7;
  transition: all 0.3s ease;
}

ul li a {
  color: $shark;
  text-decoration: none;
}
ul li ul li a {
  transition: all 0.5s ease;
}
</style>