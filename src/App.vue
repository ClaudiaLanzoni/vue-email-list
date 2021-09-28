<template>
  <div id="app">

    <div v-if="indirizzo1 != '' && indirizzo2 != '' && indirizzo3 != '' && indirizzo4 != '' 
    && indirizzo5 != '' && indirizzo6 != '' && indirizzo7 != '' && indirizzo8 != '' 
    && indirizzo9 != '' && indirizzo10 != ''">
      <ul>
        <li>{{indirizzo1.response}}</li>
        <li>{{indirizzo2.response}}</li>
        <li>{{indirizzo3.response}}</li>
        <li>{{indirizzo4.response}}</li>
        <li>{{indirizzo5.response}}</li>
        <li>{{indirizzo6.response}}</li>
        <li>{{indirizzo7.response}}</li>
        <li>{{indirizzo8.response}}</li>
        <li>{{indirizzo9.response}}</li>
        <li>{{indirizzo10.response}}</li>
      </ul>
    </div>
  
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  components: {
  
  },

  data : function () { //REGOLA COMPONENT
    return {
      indirizzo1 : "",
      indirizzo2 : "",
      indirizzo3 : "",
      indirizzo4 : "",
      indirizzo5 : "",
      indirizzo6 : "",
      indirizzo7 : "",
      indirizzo8 : "",
      indirizzo9 : "",
      indirizzo10 : "",
    }
  },

  mounted() { //This hook is not called during server-side rendering.

    console.log(axios);
    
    axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo1 = res.data;
      //console.log(res.data);
    });

     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo2 = res.data;
      //console.log(res.data);
    });
    
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo3 = res.data;
      //console.log(res.data);
    });

     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo4 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo5 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo6 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo7 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo8 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo9 = res.data;
      //console.log(res.data);
    });
     axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzo10 = res.data;
      //console.log(res.data);
    });
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  ul {
    list-style-type: none;
  }
}
</style>
