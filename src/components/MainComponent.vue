<template>
  <div>
   <jumbotron-component/>
   <sign-component/>
   <card-component/>
   <book-component/>
   <why-component/>
   <slider-component/>
   <students-component/>
  </div>
</template>

<script>
import JumbotronComponent from './JumbotronComponent.vue'
import SignComponent from './SignComponent.vue'
import CardComponent from './CardComponent.vue'
import BookComponent from './BookComponent.vue'
import WhyComponent from './WhyComponent.vue'
import SliderComponent from './SliderComponent.vue'
import StudentsComponent from './StudentsComponent.vue'

export default {
name: 'MainComponent',
components:{
JumbotronComponent,
SignComponent,
CardComponent,
BookComponent,
WhyComponent,
SliderComponent,
StudentsComponent,
}
}
</script>

<style lang="scss">

</style>