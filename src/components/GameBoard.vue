<template>
	<h1 class="hello">
		{{ msg }}
	</h1>
	<div class="row">
		<div class="col-md-6 col-lg-6 col-xl-5 mx-auto">
			<div class="row justify-content-md-center">
				<!-- cards will appear w iteration directive -->
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
				{name:'Apple',img:'apple.jpg'},
				{name:'Banana',img:'banana.jpg'},
				{name:'Orange',img:'orange.jpg'},
				{name:'Pineapple',img:'pineapple.jpg'},
				{name:'Strawberry',img:'strawberry.jpg'},
				{name:'Watermelon',img:'watermelon.jpg'},
			]
		}
	}
}
</script>
