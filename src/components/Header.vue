<template>
  <header>
    <h1 v-on:click='changeTitle' ref='h1fortitle'>{{ title }}</h1>
  </header>
</template>

<script>
import { bus } from '../main';

  export default {
    props: {
      title: {
        type: String,
        required: true,
      }
    },
    data(){
      return {

      }
    },
    methods: {
      changeTitle: function() {
        this.title = 'See the footer'
        bus.$emit('titleChanged', 'Changed by header component');
      },
    }
  }
</script>


<style scoped>
header {
  background-color: aquamarine;
  padding: 10px;
}

h1 {
  font-weight: bold;
  font-family: cursive;
  color: rgb(139, 13, 13);
  text-align: center;
}
</style>
