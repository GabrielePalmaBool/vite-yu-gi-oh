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

            <select v-model.trim="store.searchText" class="form-select w-25 ">

                <option disabled selected>Selezionare una categoria</option>

                <option v-for="(arch, i) in store.ArchList" value="i" @click.filter="$emit('filt')">
                    <SelectArc :info="arch" />
                </option>

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