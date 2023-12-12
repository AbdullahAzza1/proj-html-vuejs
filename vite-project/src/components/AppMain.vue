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
	<main>
		<div class="jumbo">
			<img src="../assets/img/image.png" alt="">
		</div>
		<div class="jumbo">
			<div>
				<p>WHO WE ARE</p>
				<h2>SENSE THE JAZZ</h2>
				<p>The Story Of Jazz And Blues Society Is The Story Of Determination, Passion, Idealism, Community, And Of
					Course, Music. Founded In 1985 And Incorporated In 1986, As A Community Based, Not-For-Profit,
					Charitable
					Arts Organization Located In Vancouver, British Columbia, The Society, From The Very Beginning, Has
					Worked
					Diligently To Establish Vancouver As A Centre For The Creation And Exchange Of Sounds And Ideas Between
					The
					Local, National And International Music Communities.</p>
				<button>read more</button>
			</div>
		</div>
		<div class="jumboVideo">
			<img src="../assets/img/assets/Video-1024x361.jpg" alt="">
			<h2 id="center">NEW MUSIC VIDEO</h2>
		</div>
		<div class="soundCategory">
			<p>WHO WE ARE</p>
			<h2>SENSE THE JAZZ</h2>
		</div>
	</main>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;
.jumbo {
	height: 35rem;
	width: 0 auto;
	background-color: black;
	display: flex;
	align-items: center;
	text-align: center;
}

img {
	width: 100%;
	height: 100%;
}

.jumboVideo {
	width: 100%;
	height: 30rem;
	position: relative;
}

#center {
	position: absolute;
	top: 50%;
	width: 100%;
	text-align: center;
}

.soundCategory {
	height: 50rem;
	background-color: black;

}

// ...qui eventuale SCSS di AppComponent
</style>
