<template>

    <div class="card-body">
        <img :src="Card.poster" alt="">
        <h5 class="card-title text-center">{{ Card.title }}</h5>
        <p class="card-text text-center">{{ Card.author }}</p>
        <p class="card-text text-center">{{ Card.year }}</p>
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

        img{
          width: 100%;
          height: 100%;
        }

        .card-title{
          color: whitesmoke;
        }

        .card-text{
          color: lightgray;
        }
    
</style>