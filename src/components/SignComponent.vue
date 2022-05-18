<template>
  <div class="sign">
    <div class="row text-center w-100">
        <div class="col-6">
            <div class="brainAcademy justify-content-center d-flex">
                <h5>Hey there, my name is John Doe. I'm the founder of the Brain Academy.</h5>
            </div>
            <img class='pt-4' src="../assets/img/sign.jpg" alt="">
        </div>
        <div class="col-6">
            <p>A wonderful serenity has taken possession of my entire soul, like these sweet mornings of spring which I enjoy with my whole heart. I am alone, and feel the charm of existence in this spot, which was created for the bliss of souls like mine. I am so happy, my dear friend, so absorbed in the exquisite sense of mere tranquil existence, that I neglect my talents. When, while the lovely valley teems with vapour around me, and the meridian sun strikes the upper surface of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'SignComponent',
}
</script>

<style lang='scss'>
.sign{
    padding: 100px 0px !important;
    width: 75%;
    margin: 0 auto;

    h5{
        width: 58%;
    }
    p{
        font-size: .80rem
    }
}
</style>