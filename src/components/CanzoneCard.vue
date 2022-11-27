<template>

  <div class="card py-2" style="width: 18rem;">

    <img :src="Card.poster" class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title text-white">{{ Card.title }}</h5>
      <span class="card-text text-white">{{ Card.author }}</span> <br>
      <span class="card-text text-white">{{ Card.year }}</span>
    </div>

  </div>
</template>
  
<script>
  
  export default {
    name: 'CanzoneCard',
    props:{
        Card: Object
    }
  }
</script>
  
<style lang="scss">

.card{
        width: calc((100% / 5) - 10px) !important;
        margin: 5px;
        background-color: #2E3A46 !important;

        img{
            width: 80%;
            margin: auto;
        }

    }
</style>