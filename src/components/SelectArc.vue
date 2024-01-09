<script >

export default {
    name: "SelectArc"
}




</script>

<template>
    <select class="form-select w-25 " aria-label="Default select example">
        <option selected>Selezionare una categoria</option>
        <option value="1">Alien</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
    </select>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header
@use '../styles/partials/variables' as *;

select {
    margin-bottom: 20px;
}
</style>