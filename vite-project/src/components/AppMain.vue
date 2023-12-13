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
		<div class="rock">
			<img src="../assets/img/assets/cms_parallax.jpg" alt="">
			<div id="center">INSTRUMENTAL ROCK
				<h2>ALBUM OUT NOW</h2>
				<button>read more</button>
			</div>
		</div>
		<div class="awards">
			<div>
				<div class="counter">
					<div>CONCERTS</div>
				</div>
			</div>
			<div>
				<div class="counter1">
					<div>HAPPY CLIENTS</div>
				</div>
			</div>
			<div>
				<div class="counter2">
					<div>MUSIC AWARDS</div>
				</div>
			</div>
			<div>
				<div class="counter3">
					<div>TOTAL SONGS</div>
				</div>
			</div>
		</div>
		<div class="bestMusic">
			<p>MUSIC BLOG</p>
			<h2>BEST MUSIC BLOG</h2>
			<div>card</div>
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

.rock {
	height: 35rem;
	width: 0 auto;
	position: relative;
}

.awards {
	height: 27rem;
	width: 0 auto;
	background-image: url(../assets/img/assets/counter_parallax.jpg);
	background-size: cover;
	display: flex;
}


@property --num {
	syntax: "<integer>";
	initial-value: 0;
	inherits: false;
}

.counter {
	animation: counter 5s infinite alternate ease-in-out;
	counter-reset: num var(--num);
	font: 800 40px system-ui;
	padding: 2rem;
}

.counter::after {
	content: counter(num);
}

@keyframes counter {
	from {
		--num: 0;
	}

	to {
		--num: 900;
	}
}

.counter1 {
	animation: counter1 5s infinite alternate ease-in-out;
	counter-reset: num var(--num);
	font: 800 40px system-ui;
	padding: 2rem;
}

.counter1::after {
	content: counter(num);
}

@keyframes counter1 {
	from {
		--num: 0;
	}

	to {
		--num: 800;
	}
}

.counter2 {
	animation: counter2 5s infinite alternate ease-in-out;
	counter-reset: num var(--num);
	font: 800 40px system-ui;
	padding: 2rem;
}

.counter2::after {
	content: counter(num);
}

@keyframes counter2 {
	from {
		--num: 0;
	}

	to {
		--num: 400;
	}
}

.counter3 {
	animation: counter3 5s infinite alternate ease-in-out;
	counter-reset: num var(--num);
	font: 800 40px system-ui;
	padding: 2rem;
}

.counter3::after {
	content: counter(num);
}

@keyframes counter3 {
	from {
		--num: 0;
	}

	to {
		--num: 1001;
	}
}

.bestMusic {
	background-color: black;
	height: 35rem;
}

// ...qui eventuale SCSS di AppComponent
</style>
