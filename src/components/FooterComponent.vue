<template>
  <div>
      <div class="container-footer">
          <div class="row py-3">
              <div class="col-3">
                  <h5>About</h5>
                  <p>Masterstudy is Education WordPress theme featured bt Learning Management System (LMS) for online education. Developed by StylemixThemes.</p>
                  <div class="d-flex gap-3">
                     <i class="fa-brands fa-facebook"></i>
                     <i class="fa-brands fa-twitter"></i>
                     <i class="fa-brands fa-instagram"></i>
                  </div>
              </div>
              <div class="col-3">
                  <h5>Contact</h5>
                  <p>USA, California 20, First Avenue, California</p>
                  <span>Tel: +1 212 458 300 32</span>  <br>
                  <span>Fax: +1 212 375 24 14</span>
                  <p class='pt-3'>info@masterstudy.com</p> 
              </div>
              <div class="col-3">
                  <h5>Pages</h5>
                  <ul class="row g-0 w-100">
                      <li class="col-6" v-for="item in footerLi" :key="item">
                          {{item.footer}}
                      </li>
                  </ul>
              </div>
              <div class="col-3">
                  <h5>Blog</h5>
                  <div class="row g-0">
                      <div class="col-12 d-flex pt-1">
                          <div class="col-4">
                              <img src="../assets/img/footer1.jpeg" alt="">
                          </div>
                          <div class="col-8">
                              <h6>Our main target is to "Developing Yourself as a Leader"</h6>
                              <span class="text-secondary size-fot">-August 9, 2018</span>
                          </div>
                      </div>
                      <div class="col-12 d-flex pt-3">
                          <div class="col-4">
                              <img src="../assets/img/footer2-.jpeg" alt="">
                          </div>
                          <div class="col-8">
                             <h6>Those Other College Expenses You Aren't Thinking About</h6>
                              <span class="text-secondary size-fot">-June 3, 2015</span> 
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
name: 'FooterComponent',
props: {
    footerLi: Array,
}
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars.scss";
div{
    background-color: $butterCup;

    .container-footer{
    width: 75%;
    margin: 0 auto;
    padding: 25px;

    h5{
        text-transform: uppercase;
    }
    p{
        font-size: 0.80rem;
    }
    ul{
        padding-left: 1rem;

        li{
        font-size: 0.73rem;
        padding-bottom: 10px
    }
    
}
    h6{
        font-size: 0.80rem;
        padding-left: 10px;
        margin-bottom: 0px;
    }
    .size-fot{
        font-size: 0.70rem;
        padding-left: 10px;
    }
}
}
</style>