<script>
import { store } from "../store.js" //state management

export default {
    name: "AppHeader",
    data() {
        return {
            store
        }
    },
    methods: {
        doThings() {
            console.log("AppComponent does things");
        }
    },
    mounted() {

    }
}
</script>

<template>
    <header>
        <img src="../" alt="">
    </header>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;
header {
    height: 6rem;
    background-color: black;
}

// ...qui eventuale SCSS di AppComponent
</style>
