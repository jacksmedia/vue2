<template>
	<h1 class="hello">
		{{ msg }}
	</h1>
	<h3>
		It doesn't work as expect... yet!
	</h3>
	<div class="row">
		<div class="col-md-6 col-lg-6 col-xl-5 mx-auto">
         <div class="row justify-content-md-center">
				<!-- cards appear from iteration directive -->
				<div v-for="card in cards" class="col-auto mb-3 flip-container" :class="{ 'flipped': card.isFlipped }" @click="flipCard(card)">
					<!-- a card -->
					<div class="memorycard" v-bind:key="type">

						<div class="front border rounded">
							<img width="100"
								height="150"
								:src="require(`../assets/${card.img}`)"
							/>
						</div>
						{{ card.name }}
						<div class="back border rounded">
							<img width="100"
								height="150"
								src="/assets/logo.png"
							/>
						</div>

					</div> 
				</div>
			</div>
		</div>
	</div>
</template>
<!-- why are you still building w Reactjs? 🤷 -->
<script>
export default {
	name: 'GameBoard',
	props: {
		msg: String
	},
	data() {
		return {
			cards: [
				{name:'Apple',img:'apple-card.jpg',},
				{name:'Banana',img:'banana-card.jpg',},
				{name:'Orange',img:'orange-card.jpg',},
				{name:'Pineapple',img:'pineapple-card.jpg',},
				{name:'Strawberry',img:'strawberry-card.jpg',},
				{name:'Watermelon',img:'watermelon-card.jpg',},
			]
		}
	},
	created(){
		this.cards.forEach((card) => {
			Vue.set(card.isFlipped = false)
		});
	},

	methods:{
		flipCard(card){
			card.isFlipped = true;
		}
	}
}
</script>

<style>
.flip-container {
  -webkit-perspective: 1000;
  -moz-perspective: 1000;
  -o-perspective: 1000;
  perspective: 1000;
  min-height: 120px;
  cursor: pointer;
}
.front,
.back {
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  -o-backface-visibility: hidden;
  backface-visibility: hidden;
  -webkit-transition: 0.6s;
  -webkit-transform-style: preserve-3d;
  -moz-transition: 0.6s;
  -moz-transform-style: preserve-3d;
  -o-transition: 0.6s;
  -o-transform-style: preserve-3d;
  -ms-transition: 0.6s;
  -ms-transform-style: preserve-3d;
  transition: 0.6s;
  transform-style: preserve-3d;
  top: 0;
  left: 0;
  width: 100%;
}
.back {
  -webkit-transform: rotateY(-180deg);
  -moz-transform: rotateY(-180deg);
  -o-transform: rotateY(-180deg);
  -ms-transform: rotateY(-180deg);
  transform: rotateY(-180deg);
  position: absolute;
}
.flip-container.flipped .back {
	-webkit-transform: rotateY(0deg);
	-moz-transform: rotateY(0deg);
	-o-transform: rotateY(0deg);
	-ms-transform: rotateY(0deg);
	transform: rotateY(0deg);
}
.flip-container.flipped .front {
	-webkit-transform: rotateY(180deg);
	-moz-transform: rotateY(180deg);
	-o-transform: rotateY(180deg);
	-ms-transform: rotateY(180deg);
	transform: rotateY(180deg);
}
</style>
