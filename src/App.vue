<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import MainComponent from './components/MainComponent.vue';
export default {
  data(){
    return {}
  },
  components:{
    HeaderComponent,
    FooterComponent ,
    MainComponent 
  }
}
</script>

<template>
  <HeaderComponent />

  <MainComponent />

  <FooterComponent />


</template>

<style scoped>
</style>
