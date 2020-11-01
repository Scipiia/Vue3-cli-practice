<template>
	<div class="cards">
		<div class="scene">
			<div 
				class="card" 
					:class="{flipped}"
					@click="flippedSee"
				>
				<div class="card__face card__face--front"> 
					<span class="card-name">{{agent_data.name}}</span>
					<h4 class="card-role">\\{{agent_data.role}}</h4>
					<p class="card-bio">{{agent_data.bio}}</p>
					<button @click="$emit('toggle')">Удалить</button>

					<!--тут передаю родителю, что при клике надо изменить isActive-->
					<button v-on:click="$emit('flipped')">See</button>
				</div>
				<div class="card__face card__face--back"><img class="card-image" v-bind:src="require('../assets/' + agent_data.image)" alt=""></div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	//props: {
	//	agent_data: {
	//		type: Object,
	//		default() {
	//			return {}
	//		}
	//	}
	//},
	//props: ['agent_data'],
	props: {
		agent_data: {
			type: Object,
			required: true
		},
		flipped_card: {   //принял дочернии элемент, который уже изменил состояние, но куда дальше
			type: Boolean,	//не могу понять :(
			required: true
		}
	},
	methods: {
		flippedSee() {
			this.flipped = !this.flipped
			console.log(this.flipped)
		}
	},
	computed: {
		
	},
	data() {
		return {
			flipped: false //это был хитрый ход и скорее всего не правильный, тк надо было передать родителю,
											//что состояние изменилось, от родителя получить изменения и перевернуть карточку
											//я пытался сделать правильно, но чет не пошло, но еще лучше, если бы использовал vuex,
											//но пока vuex где то там понимаю, но не могу применить
		}
	}
	//computed: {
	//	isActive() {
	//		return {
	//			isActive = true
	//		}
	//	}
	//}
}
</script>

<style scoped>

	.cards {
		display: inline-block;
		margin-left: 10px;
		text-align: center;
	}


	.card-image {
		width: 300px;
		height: 450px;
		perspective: 1000px;
	}

	.scene {
	width: 300px;
	height: 450px;
	perspective: 1000px;
}

.card {
	width: 300px;
	height: 450px;
	position: relative;
	transition: transform 1s;
	transform-style: preserve-3d;
}

.card-name{
	font-size: 22px;
}

.card-role{
	margin-top: 50px;
	font-size: 23px;
}

.card-bio{
	line-height: 25px;
}

.card__face {
	position: absolute;
	width: 300px;
	height: 450px;
	backface-visibility: hidden;
}

.card__face--front {
	background: rgb(185, 15, 15);
}

.card__face--back {
	width: 300px;
	height: 450px;
	background: white;
	transform: rotateY(180deg);
}

.card.flipped {
	transform: rotateY(180deg);
}

</style>