<template>
  <div>
    <app-header v-bind:title='title'></app-header>
    <app-programmers v-bind:programmers='programmers'></app-programmers>
    <app-footer v-bind:title='title'></app-footer>
  </div>
</template>

<script>
import Header from './components/Header';
import Programmers from './components/Programmers';
import Footer from './components/Footer';

  export default {
    components: {
      'app-header': Header,
      'app-programmers': Programmers,
      'app-footer': Footer,
    },
    data(){
      return {
        programmers: [
          {name: 'Raniket', speciality: 'Data Scientist', show: false},
          {name: 'Ricky', speciality: 'Software Developer', show: false},
          {name: 'Logan', speciality: 'Solution Architect', show: false},
          {name: 'Tango', speciality: 'Machine Learning', show: false},
        ],
        title: 'Programmers Yard'
      }
    },
    methods: {
    } 
  }
</script>


<style scoped>

</style>
