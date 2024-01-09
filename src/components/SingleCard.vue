<script>

export default {
    name: "SingleCard",

    props: {
        info: Object
    }

}




</script>

<template>
    <div class="backgroundC">
        <div class="card">
            <img :src="info.card_images[0].image_url" alt="">
            <h4>{{ info.name }}</h4>
            <h5>{{ info.archetype }}</h5>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.backgroundC {

    padding: 20px;

    .card {
        background-color: $bg-color;
        text-align: center;

        h4 {
            text-transform: capitalize;
            font-size: 15px;
            color: $bg-color1;
        }

        h5 {
            font-size: 15px;
        }
    }


}
</style>