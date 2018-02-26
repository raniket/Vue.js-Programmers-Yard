<template>
  <div id='programmers'>
    <ul>
      <li v-for="programmer in programmers">
        <h1 v-on:click="programmer.show = !programmer.show">{{ programmer.name }}</h1>
        <h3 v-show="programmer.show">{{ programmer.speciality }}</h3>
      </li>
    </ul>
    <button v-on:click='deleteProgrammer'>delete programmer</button>
  </div>
</template>

<script>
export default {
  props: {
    programmers: {
      type: Array,
      required: true,
    },
  },
  data(){
    return {

    }
  },
  methods: {
    deleteProgrammer(){
      this.programmers.pop();
    }
  },
}
</script>

<style scoped>
#programmers{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
}
</style>
