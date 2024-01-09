<script >

export default {
    name: "SelectArc",

    props: {
        info: Object
    }
}

</script>

<template>
    <option>{{ info.archetype_name }}</option>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header
@use '../styles/partials/variables' as *;
</style>