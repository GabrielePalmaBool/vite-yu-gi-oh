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

      let myURL = store.apiURL


      //Se è stato selezionato qualcosa dal selettore
      if (store.searchText !== "") {
        myURL = `https://db.ygoprodeck.com/api/v7/cardinfo.php?${store.Arc}=${store.searchText}`
      }

      console.log(myURL);
      //prima chiamata axios
      axios.get(myURL).then((res => { store.CardList = res.data.data; console.log(store.CardList); })).catch((err) => { console.log("Errori", err); });

      //Seconda chiamta axios
      axios.get(store.apiURL2).then((res => { store.ArchList = res.data; console.log(store.ArchList); })).catch((err) => { console.log("Errori", err); });
    }
  },

  created() {
    this.getCards();
  }

}
</script>

<template>
  <Myheader />
  <Mymain @filter="getCards" />
  <Myfooter />
</template>

<style lang="scss" >
@use './styles/general.scss';
</style>
