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
                <div class="row row-cols-5 ">
                    <div v-for="card in store.CardList" :key="card" class="col p-2">
                        <SingleCard :info="card" />
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
    padding-bottom: 50px;

    select {
        margin-bottom: 20px;
    }

    .sub {
        background-color: $bg-color1;

    }
}
</style>