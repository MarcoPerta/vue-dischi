<template>
    <header>
      <div class="d-flex justify-content-start">
        <img class="align-self-center mx-2" src="../assets/logo-small.svg" alt="">
      </div>
    </header>
</template>
  
  <script>
  
  export default {
    name: 'HeaderComp',
    props:["methodEmitApp"]
  }
  </script>
  
  <style lang="scss">
  header{
    height: 10vh;
    background-color: #2E3A46;
    div{
      height: 100%;
      img{
        width: 50px;
        height: 50px;
      }
    }
  }
  </style>