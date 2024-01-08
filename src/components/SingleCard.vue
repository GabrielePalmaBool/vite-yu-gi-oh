<script>

export default {
    name: "SingleCard"
}




</script>

<template>
    <div class="background">
        <div class="card">
            <img src="" alt="">
            <h4>nome carta</h4>
            <h5>tipo carta</h5>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.background {
    background-color: $bg-color;
}

h4 {
    text-transform: capitalize;
}
</style>