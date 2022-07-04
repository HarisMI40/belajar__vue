<template>
 <h1>{{angka}}</h1>
 <div>
   <img :src="foto" width="500"/>
 </div>
 <button v-on:click="changeImage">Change Image</button>
</template>

<script>
const fotoss = [
     {
      id: 1, 
      url : "https://media.suara.com/pictures/653x366/2021/12/28/11513-ilustrasi-kucing-dengan-mata-beda-warna-pixabaybaran65.jpg"
      },
      {
        id: 2, 
        url : "https://cdn1-production-images-kly.akamaized.net/nQF66ic6xRDS2tL6yNU3nBrFBqQ=/1200x1200/smart/filters:quality(75):strip_icc():format(jpeg)/kly-media-production/medias/3209208/original/001184800_1597393099-kucingjahilcov.jpg"
      },
      {
        id: 3, 
        url : "https://www.ruparupa.com/blog/wp-content/uploads/2021/02/Screen-Shot-2021-02-05-at-11.53.27-1024x622.png"
      }
];

var angka = 0;

export default {
  name: 'App',
  components: {
  },
  data() {
    return{
      nama : " ini nama",
      angka : 0,
      foto : fotoss[angka].url
    }
  },
  methods : {
    changeImage(){
      if(this.angka < 2){
        this.foto = fotoss[this.angka + 1].url;
        this.angka = this.angka + 1;
        
      }else{
        this.angka = 0;
        this.foto = fotoss[this.angka].url;
      }
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

img{
    background-size: cover;
    height: 500;
    height: 304px;
    background-position: center;
}
</style>
