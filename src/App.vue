<!--    Popular Tv Shows
        Name: Juan Vazquez
        Teacher: Kirsten Markley
        Class: cis-131-w01
        Date: 12/6/20
-->
<template>
  <div id="app">
    <!--components placed into main "app" div-->
    <Header headerTitle="Popular Tv Shows"/>
    <Card v-bind:tvArray="tvObj"/>
  </div>
</template>

<script>
//imported components
import Header from './components/Header.vue'
import Card from './components/Card.vue'
import axios from 'axios'


export default {
  name: 'App',
  components: {
    Header,
    Card
  },
  data(){
    return{
      tvObj: ""
    }
  },
  //axios api call
  mounted(){
    axios.get('https://api.themoviedb.org/3/tv/popular?api_key=c4e63ad17769d8bb1a2163ce73a3d827&language=en-US&page=1')
    .then ((res) => {
      //json array stored into tvObj
      this.tvObj = res.data.results.slice(0,4);
      
      console.log(this.tvObj)
    })
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
