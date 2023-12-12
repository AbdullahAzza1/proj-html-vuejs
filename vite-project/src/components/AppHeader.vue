<script>
import { store } from "../store.js" //state management

export default {
    name: "AppHeader",
    props: ["links"],
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
        <img src="../assets/img/assets/Logo.png" alt="">
        <div class="menu">
            <a v-for="link in links" :href="link.link">{{ link.label }}</a>
        </div>
    </header>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;
header {
    height: 6rem;
    background-color: black;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    width: 100%;
}

header a {
    padding: 0 1rem;
    color: white;
    text-decoration: none;
}


// ...qui eventuale SCSS di AppComponent
</style>
