<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
   
   <!--  <router-link to="/kelas">Data Kelas  </router-link>
    <router-link to="/siswa">Data Siswa</router-link>
    <router-view/><br><br> -->

    <h1>{{ name }}</h1>
    <input v-model="name" placeholder="Masukan Nama"><br><br>
    <p>Nilai Anda : {{ total }}</p> 
    <button v-on:click="button">Click Me!</button>

    <p><b>1) Pulau Lombok berada di Provinsi ? </b></p>
    <input type="radio" value="NTB" v-model="soal1">
    Nusa Tenggara Barat &nbsp &nbsp
    <input type="radio" value="NTT" v-model="soal1">
    Nusa Tenggara Timur &nbsp &nbsp
    <input type="radio" value="Kalbar" v-model="soal1">
    Kalimantan Barat &nbsp &nbsp
    <input type="radio" value="Kalteng" v-model="soal1">
    Kalimantan Tengah 
    <input type="radio" value="SulBarat" v-model="soal1">
    Sulawesi Barat <br><br>

    <p><b>2) 7 + 10 x 3 = </b></p>
   <input type="radio" value="51" v-model="soal2">
   51 &nbsp &nbsp
   <input type="radio" value="37" v-model="soal2">
   37 &nbsp &nbsp
   <input type="radio" value="100" v-model="soal2">
   100 &nbsp &nbsp
   <input type="radio" value="53" v-model="soal2">
   53 <br><br>

   <p><b>3) Manakah hewan dibawah ini yang termasuk kedalam <i>OMNIVORA</i> ?</b></p>
   <input type="radio" value="Macan" v-model="soal3">
   Macan  &nbsp &nbsp
   <input type="radio" value="Buaya" v-model="soal3">
   Buaya  &nbsp &nbsp
   <input type="radio" value="Badak" v-model="soal3">
   Badak  &nbsp &nbsp
   <input type="radio" value="Beruang" v-model="soal3">
   Beruang &nbsp &nbsp
   <input type="radio" value="Anoa" v-model="soal3">
   Anoa 

  </div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data() {
    return {
      name : '',
      soal1 :'',
      soal2 :'',
      soal3 : '', 
      total : 0
    }
    },
  methods: {
    button(){
      if (this.soal1 == 'NTB' && this.soal2 == '37' && this.soal3 == 'Beruang') {
        this.total=+3
      }
      else if(this.soal1 == 'NTB' && this.soal2 == '37') {
        this.total=+2
      }
      else if(this.soal1 == 'NTB' && this.soal3 == 'Beruang') {
        this.total=+2
      }
      else if(this.soal2 == '37' && this.soal3 == 'Beruang') {
        this.total=+2
      }
      else if (this.soal1 == 'NTB') {
        this.total=+1
      }
      else if(this.soal2 == '37') {
        this.total=+1
      }
      else if (this.soal3 == 'Beruang') {
        this.total=+1
      }
      else{this.total = 0}
    }
  },
  components: {
    HelloWorld
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
