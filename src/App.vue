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
    <button v-on:click="result">Click Me!</button>

    <p><b>1. Tahun berapa Indonesia merdeka?</b></p>
    <input type="radio" value="1998" v-model="one">
    1998 &nbsp &nbsp
    <input type="radio" value="1945" v-model="one">
    1945 &nbsp &nbsp
    <input type="radio" value="1954" v-model="one">
    1954 &nbsp &nbsp
    <input type="radio" value="1970" v-model="one">
    1970 <br><br>

    <p><b>2. Berapakah hasil dari 9 x 11 + 2?</b></p>
   <input type="radio" value="99" v-model="two">
   99 &nbsp &nbsp
   <input type="radio" value="100" v-model="two">
   100 &nbsp &nbsp
   <input type="radio" value="101" v-model="two">
   101 &nbsp &nbsp
   <input type="radio" value="102" v-model="two">
   102 <br><br>

   <p><b>3. Manakah yang termasuk alat musik yang dipetik?</b></p>
   <input type="radio" value="Suling" v-model="three">
   Suling  &nbsp &nbsp
   <input type="radio" value="Drum" v-model="three">
   Drum  &nbsp &nbsp
   <input type="radio" value="Biola" v-model="three">
   Biola  &nbsp &nbsp
   <input type="radio" value="Gitar" v-model="three">
   Gitar

  </div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data() {
    return {
      name : '',
      one :'',
      two :'',
      three : '', 
      total : 0
    }
    },
  methods: {
    result(){
      if (this.one == '1945' && this.two == '101' && this.three == 'Gitar') {
        this.total=+3
      }
      else if(this.one == '1945' && this.two == '101') {
        this.total=+2
      }
      else if(this.one == '1945' && this.three == 'Gitar') {
        this.total=+2
      }
      else if(this.two == '101' && this.three == 'Gitar') {
        this.total=+2
      }
      else if (this.one == '1945') {
        this.total=+1
      }
      else if(this.two == '101') {
        this.total=+1
      }
      else if (this.three == 'Gitar') {
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
