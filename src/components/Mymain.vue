<script >
import SingleCard from './SingleCard.vue'

import SelectArc from './SelectArc.vue'

//importo store
import { store } from '../store'


export default {
    name: "Mymain",

    components: {
        SingleCard,
        SelectArc
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

            <SelectArc />
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

    .sub {
        background-color: $bg-color1;

    }
}
</style>