<script >

//importo libreria axios
import axios from 'axios'

//importo componenti figli
import Myheader from './components/Myheader.vue'
import Mymain from './components/Mymain.vue'
import Myfooter from './components/Myfooter.vue'

//importo store
import { store } from './store'

export default {

  components: {
    Myheader,
    Mymain,
    Myfooter
  },

  data() {
    return {
      store,
    }

  },

  methods: {
    getCards() {
      axios
        .get(store.apiURL)
        .then((res => {

          store.CardList = res.data.data;

          console.log(store.CardList);

        }))
        .catch((err) => {
          console.log("Errori", err);
        });
    }
  },

  created() {
    this.getCards();
  }

}
</script>

<template>
  <Myheader />
  <Mymain />
  <Myfooter />
</template>

<style lang="scss" >
@use './styles/general.scss';
</style>
