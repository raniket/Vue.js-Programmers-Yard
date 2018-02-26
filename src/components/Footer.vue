<template>
  <footer>
    <p>{{ copyright }} {{ title }}</p>
  </footer>
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
    data() {
      return {
        copyright: 'copyright 2018 ',
      }
    },
    created() {
      bus.$on('titleChanged', (data) => {
        this.title = data;
      });
    }
  }
</script>

<style scoped>
footer {
  background-color: rgb(71, 62, 62);
  padding: 10px;
}

p {
  color:aquamarine;
  text-align: center;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
</style>
