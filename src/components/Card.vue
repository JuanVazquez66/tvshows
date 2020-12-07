<!--    Popular Tv Shows
        Name: Juan Vazquez
        Teacher: Kirsten Markley
        Class: cis-131-w01
        Date: 12/6/20
-->
<!--new component for Card-->
<template>
    <div class="card" style="width: 18rem;">
        <div class="show" v-for="show in tvArray" v-bind:key="show.id">    
            <img v-bind:src="'https://image.tmdb.org/t/p/w300//' + show.poster_path" class="card-img-top">
            <div class="card-body"> 
                <h4 class="card-title">{{show.name}}</h4>        
                <p class="card-text">{{show.overview}}</p>   
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ['tvArray']
}
</script>

<style scoped>
    .card{
        
        display: inline-flex;
        margin-right: 1000px;
        margin-top: 20px;
        
    }
    .show{
        padding-left: 10px;
        padding-right: 10px;
    }
</style>