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
        <div>
            <h1>footer</h1>
        </div>
    </header>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;
header {
    height: 4rem;
    background-color: black;
}

// ...qui eventuale SCSS di AppComponent
</style>
