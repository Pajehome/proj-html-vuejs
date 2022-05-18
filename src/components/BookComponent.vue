<template>
  <div class="bg-book">
     <div class="container-book">
         <div class="row text-center w-100">
        <div class="col-6 pt-5">
            <div class="justify-content-center d-flex">
                <h5>Get My Exclusive Investing Book just for $19.50</h5>
            </div>
            <div class="justify-content-center d-flex pt-3">
                <p>Vestibulum imentum eu urna vel cusus. Aenean vehicula quam quam, vitae pellestenque urna elementum cursus.</p>
            </div>

            <img class='pt-2 w-25' src="../assets/img/amazon.png" alt="">
        </div>
        <div class="col-6">
            <img class='w-75' src="../assets/img/book.png" alt="">
        </div>
    </div>
     </div> 
  </div>
</template>

<script>
export default {
name: 'BookComponent',
}
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
.bg-book{
    background-image: url(../assets/img/biblio.jpg);
}
.container-book{
    padding-top: 20px;
    width: 75%;
    margin: 0 auto;

    h5{
        width: 58%;
        color: $butterCup;
    }
    p{
        width: 65%;
        font-size: .80rem;
        color: $white;
    }
}
</style>