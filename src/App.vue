<template>
 <h1>{{nama}}</h1>
 <img :src="foto[0].url"/>
 <button v-on:click="updateName">Change Name</button>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return{
      nama : " ini nama",
      foto : [
        {id: 1, url : "https://media.suara.com/pictures/653x366/2021/12/28/11513-ilustrasi-kucing-dengan-mata-beda-warna-pixabaybaran65.jpg"}
      ]
    }
  },
  methods : {
    updateName(){
      this.nama = "update name"
    }
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
  margin-top: 60px;
}
</style>
