<script>
  import axios from 'axios';
  import CardComponent from './CardComponent.vue';
  export default {
   
    data(){
      return {
        projects:[],
      }
    },
    components:{
      CardComponent

    },

    mounted() {
      axios.get('http://127.0.0.1:8000/api/project')
        .then(res =>{
          this.projects =  res.data.results;
        });
    },
  }
</script>

<template>
  <div>
    <h1>Lista progetti</h1>
  </div>

  <div class="card-container">   
    <CardComponent
      v-for="(project, index) in projects" 
      :key="index"
      :projectObj="project"
    />
  </div>
</template>

<style >
  .card-container{
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding-inline:20px ;
  }
</style>