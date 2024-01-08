<script >
import SingleCard from './SingleCard.vue'

//importo store
import { store } from '../store'


export default {
    name: "Mymain",

    components: {
        SingleCard
    },

    data() {
        return {
            store,
        }
    }
}




</script>

<template>
    <div class="background">

        <main class="container ">

            <select class="form-select w-25 " aria-label="Default select example">
                <option selected>Selezionare una categoria</option>
                <option value="1">Alien</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>

            <div class="container sub">
                <div class="row">
                    <div v-for="card in store.CardList" class="col-5 p-2 card">
                        <SingleCard />
                    </div>

                </div>
            </div>

        </main>
    </div>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header
@use '../styles/partials/variables' as *;

.background {
    background-color: $bg-color;
}

main {
    padding-top: 50px;
}



.sub {
    background-color: $bg-color1;

    .card {

        background-color: red;
    }

}
</style>