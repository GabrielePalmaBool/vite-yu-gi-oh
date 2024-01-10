<script >

export default {
    name: "Myfooter"
}




</script>

<template>
    <footer class="container">

        <h2>No Footer</h2><img src="/rick-astley-dance.gif" class="gif" alt="Footer non presente">
        <h2>No Footer</h2>
    </footer>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header
@use '../styles/partials/variables' as *;


.gif {
    width: 15%;
    margin-left: 12%;

    vertical-align: middle;
}

h2 {
    margin-left: 17%;
    display: inline-block;
}
</style>