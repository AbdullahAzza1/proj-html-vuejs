<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

import axios from 'axios'; //importo Axios
import { store } from "./store.js" //state management


export default {
	components: {
		AppHeader,
		AppMain,
		AppFooter
	},
	data() {
		return {
			store,
			menuLinks: [
				{
					id: 1,
					label: 'Home',
					link: '#'
				},
				{
					id: 2,
					label: 'blog',
					link: '#'
				},
				{
					id: 3,
					label: 'events',
					link: '#'
				},
				{
					id: 4,
					label: 'gallery',
					link: '#'
				},
				{
					id: 5,
					label: 'about us',
					link: '#'
				},
				{
					id: 6,
					label: 'contacts',
					link: '#'
				},
				{
					id: 7,
					label: 'shop',
					link: '#'
				},
			],
			card: [
				{
					id: 1,
					image: "../assets/img/assets/",
					text: '',
				}
			]
		}
	},
	mounted() {
		this.doThings();

		// axios.get("indirizzo").then(risultato => {
		// 	console.log(risultato);
		// }).catch(errore => {
		// 	console.error(errore);
		// });
	},
	methods: {
		doThings() {
			console.log("App.vue does things");
		}
	}
}
</script>

<template>
	<header>
		<AppHeader :links="menuLinks" />
	</header>
	<main>
		<AppMain />
	</main>
	<footer>
		<AppFooter />
	</footer>
</template>

<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped


@use './styles/general.scss';
</style>

<style scoped lang="scss">
// importo variabili
@use './styles/variabili/variabili.scss' as *;

// ...qui eventuale SCSS di App.vue
</style>
