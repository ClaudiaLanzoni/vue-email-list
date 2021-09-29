<template>
  <div id="app">

    <div>
      <ul>
        <li v-for="(element, index) in indirizzi" :key="index">
          {{element.response}}
        </li>
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
      indirizzi : []
    }
  },

  mounted() { //This hook is not called during server-side rendering.

    for (var i = 0; i < 10; i++) {
        axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
    .then(res => {
      
      this.indirizzi.push(res.data);
      //console.log(indirizzo);

    });
    }
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