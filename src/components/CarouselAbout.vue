<template>
	<div class="wrapper">
		<div 
			class="carousel-about"
			:style="{'margin-left': '-' + (100 * currentSlideIndex) + '%' }"
		>
			<CarouselItem
			v-for="item in carousel_data"
			:key="item.id"
			v-bind:item_data="item"
			:imageSlide="true"
		/>
		</div>
		<button @click="prevSlide">Prev</button>
		<button @click="nextSlide">Mext</button>
	</div>
</template>

<script>
import CarouselItem from './CarouselItem'

export default {
	name: 'carousel-about',
	components: {
		CarouselItem
	},
	props: {
		carousel_data: {
			type: Array,
			default: () => []
		},
		interval: {
			type: Number,
			degault: 0
		}
	},
	methods: {
		prevSlide() {
			if(this.currentSlideIndex > 0) {
				this.currentSlideIndex--
			}
		},
		nextSlide() {
			if(this.currentSlideIndex >= this.carousel_data.length - 1) {
				this.currentSlideIndex = 0
			} else {
			this.currentSlideIndex++
			}
		}
	},
	mounted() {
		if (this.interval > 0) {
			let vm = this;
			setInterval(function () {
				vm.nextSlide()
			}, vm.interval)
		}
	},
	data() {
		return {
			currentSlideIndex: 0
		}
	}
}
</script>

<style scoped>

	.wrapper {
		margin: auto;
		max-width: 800px;
		overflow: hidden;
	}

	.carousel-about {
		display: flex;
		transition: all ease 0.5s;
	}


</style>