<template>
  <div id="app">
    <header>
       <header-component :headerLi="myData.headerData"/>
    </header>

    <main>
      <main-component/>
    </main>
  
    <footer>
       <footer-component :footerLi="myData.footerData"/>
    </footer>
  
  </div>
</template>

<script>

import dati from './dati.json';
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
  data(){
    return{
      myData: dati
    }
  },
}
</script>

<style  lang="scss">
@import "./assets/styles/general.scss";

</style>
