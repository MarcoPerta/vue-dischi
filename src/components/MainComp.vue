<template>
    <main>
        <div class="container d-flex flex-wrap">
            
            <CanzoneCard v-for="(elem,index) in albums" :key="index" :Card="elem"/>
            
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
            albums: [],
            arrayGeneri: []
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
                    this.albums.forEach((singoloAlbum) => {
                        if(!this.arrayGeneri.includes(singoloAlbum.genre)){
                            this.arrayGeneri.push(singoloAlbum.genre)
                        }
                    });

                    this.$emit('emitGeneri',this.arrayGeneri)
                })
        }
    }
}

</script>
  
<style lang="scss">
main{
    background-color: #1E2D3B;
    // height: 90vh;
    padding: 50px;
    
}
</style>