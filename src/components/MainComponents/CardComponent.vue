<script>
  export default {
    data(){
      return{
      }
    },
    props:{
      projectObj:{
        type:Object,
        default:{}
      },
    },
  }
</script>

<template>
  <div class="card">
    <div class="card-img-wrapper">
      <img :src="projectObj.preview" :alt="projectObj.title">
    </div>
    <div class="description">
      <h2>
        Titolo progetto: <span>{{ projectObj.title }}</span>
      </h2>
      <h3>
        Fatto in collaborazione con:
        <span>{{ projectObj.collaborators }}</span> 
      </h3>
    </div>
      <div class="action-wrapper">
        <button href="">vedi</button>
      </div>
  </div>
</template>

<style >
  .card {
    width: calc((100% - 60px)/4);
    margin-block: 20px;
    box-shadow: 10px 5px 5px rgba(0, 0, 0, 0.3);
    border: 1px solid #ccc;
    border-radius: 10px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }

  .card .description {
    padding-inline: 10px;
  }

  .card h2{
    font-size: 20px;
  }

  .card h2 span,
  .card h3 span{
    color: #aaa;
  }

  .card .card-body{
    padding-inline: 10px;
  }

  .card .card-img-wrapper img{
    width: 100%;
    object-fit: cover;
  }

  .card .action-wrapper {
    height: 100%;
    display:flex;
    align-items: flex-end;
    justify-content: center;
    padding: 10px 0;
  }

  .card button {
    padding: 15px 30px;
    border-radius: 10px;
    background-color: aquamarine;
    border: 0;

    cursor: pointer;
    display: inline-block;
    margin-top: 10px;
    text-decoration: none;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    transition: background-color 200ms ease-in-out,
                color 200ms ease-in-out;
  }

  .card button:hover {
    background-color: rgb(14, 131, 92);
    color: #fff;
  }

  @media screen and (max-width:1000px){
    .card {
      width: calc((100% - 40px)/3);
    }
  }

  @media screen and (max-width:700px){
    .card {
      width: calc((100% - 20px)/2);
    }
  }

  @media screen and (max-width:600px){
    .card {
      width:80%;
      margin-inline: auto;
    }
  }
</style>