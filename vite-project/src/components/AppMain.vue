<script>
import { store } from "../store.js" //state management

export default {
	name: "AppMain",
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
	<div>
		<h1>main</h1>
	</div>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;

// ...qui eventuale SCSS di AppComponent
</style>
