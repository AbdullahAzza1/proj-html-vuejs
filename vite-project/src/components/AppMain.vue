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

		window.onload = function () {
			let slides =
				document.getElementsByClassName('carousel-item');

			function addActive(slide) {
				slide.classList.add('active');
			}

			function removeActive(slide) {
				slide.classList.remove('active');
			}

			addActive(slides[0]);
			setInterval(function () {
				for (let i = 0; i < slides.length; i++) {
					if (i + 1 == slides.length) {
						addActive(slides[0]);
						setTimeout(removeActive, 350, slides[i]);
						break;
					}
					if (slides[i].classList.contains('active')) {
						setTimeout(removeActive, 350, slides[i]);
						addActive(slides[i + 1]);
						break;
					}
				}
			}, 1500);
		};
	}
}
</script>

<template>
	<main>
		<div class="jumbo">
			<div class="carousel">
				<div class="carousel-item">
					<div class="slide-image" style="background-image:  url(../assets/img/image.png);">
					</div>
					<div>INSTRUMENTAL ROCK</div>
				</div>
				<div class="carousel-item">
					<div class="slide-image" style="background-image: url(../assets/img/image(1).png);">
					</div>
				</div>
			</div>
		</div>
		<div class="cards">
			<div>
				<img src="../assets/img/speaker.svg" alt="">
				<h3>ORIGINAL IDEAS</h3>
				<div>Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.</div>
			</div>
			<div>
				<img src="../assets/img/disc.svg" alt="">
				<h3>ORIGINAL IDEAS</h3>
				<div>Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.</div>
			</div>
			<div>
				<img src="../assets/img/headphones.svg" alt="">
				<h3>ORIGINAL IDEAS</h3>
				<div>Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.</div>
			</div>
		</div>
		<div class="jumboStory">
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
			<h2>NEW MUSIC VIDEO</h2>
		</div>
		<div class="soundCategory">
			<p>WHO WE ARE</p>
			<h2>SENSE THE JAZZ</h2>
		</div>
		<div class="rock">
			<div>INSTRUMENTAL ROCK
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
	background-image: url(../assets/img/image.png);
	background-size: cover;
}

.cards {
	display: flex;
	justify-content: space-around;
	position: absolute;
	width: 100%;
	top: 61%;
}

.cards>div {
	background-color: rgb(33, 33, 33);
	height: 47vh;
	width: 30vw;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	padding: 35px
}

.cards img {
	width: 25%;
	color: white;
}

.jumboStory {
	height: 35rem;
	width: 0 auto;
	background-color: black;
	display: flex;
	align-items: center;
	text-align: center;
	background-size: cover;
}

img {
	width: 100%;
	height: 100%;
}

.jumboVideo {
	background-image: url(../assets/img/assets/Video-1024x361.jpg);
	height: 30rem;
	background-size: cover;
	display: flex;
	justify-content: center;
	align-items: center;
}



.soundCategory {
	height: 50rem;
	background-color: black;

}

.rock {
	height: 35rem;
	background-image: url(../assets/img/assets/cms_parallax.jpg);
	background-size: cover;
	display: flex;
	align-items: center;
}

.awards {
	height: 27rem;
	background-image: url(../assets/img/assets/counter_parallax.jpg);
	background-size: cover;
	display: flex;
	align-items: center;
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



.carousel {
	position: relative;
	width: 100%;
	height: 100%;
	overflow: hidden;
}

.carousel-item .slide-image {
	width: 270px;
	height: 160px;
	background-size: cover;
	background-repeat: no-repeat;
}

.carousel-item {
	position: absolute;
	width: 100%;
	height: 270px;
	border: none;
	top: 96px;

}

.carousel-item.active {
	left: 0;
	transition: all 0.3s ease-out;
}

.carousel-item div {
	height: 100%;
}

.red {
	background-color: red;
}

.green {
	background-color: green;
}

.yellow {
	background-color: yellow;
}

.violet {
	background-color: violet;
}
</style> // ...qui eventuale SCSS di AppComponent