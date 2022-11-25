<template>
    <main>
        <div class="container d-flex flex-wrap">
            <div class="card flex-row">
                <CanzoneCard v-for="(elem,index) in albums" :key="index" :Card="elem"/>
            </div>
        </div>
    </main>
</template>
  
<script>
import CanzoneCard from './CanzoneCard.vue'
import axios from 'axios'
  
export default {
    name: 'MainComp',
    components: {
        CanzoneCard
    },
    data() {
        return {
            albums: ''
        }
    },
    mounted() {
        this.getAlbums();
    },
    methods: {
        getAlbums() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then((response) => {
                    // console.log(response.data.response)
                    this.albums = response.data.response
                    // console.log(this.albums)
                })
        }
    }
}

</script>
  
<style lang="scss">
main{
    background-color: #1E2D3B;
    height: 90vh;
    padding: 50px;
    .container{
        .card{
        width: calc(100% / 5);
        background-color: #2E3A46;
    }
    }
}
</style>