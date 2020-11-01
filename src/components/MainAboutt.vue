<template>
	<div class="main-about">
		<CarouselAbout
			v-bind:carousel_data="gallery"
			:interval="3000"
		/>
	</div>
</template>

<script>
import CarouselAbout from '../components/CarouselAbout'

export default {
	name: 'MainAbout',
		components: {
		CarouselAbout
	},
	data() {
		return {
			gallery : [
				{
					id: 1,
					name: '1img',
					image: '1.jpg'
				},
				{
					id: 2,
					name: '2img',
					image: '2.jpg'
				},
				{
					id: 3,
					name: '3img',
					image: '3.jpg'
				},
				{
					id: 4,
					name: '4img',
					image: '4.jpg'
				},
				{
					id: 5,
					name: '5img',
					image: '5.jpg'
				},
				{
					id: 6,
					name: '6img',
					image: '6.jpg'
				},
				{
					id: 7,
					name: '7img',
					image: '7.jpg'
				},
				{
					id: 8,
					name: '8img',
					image: '8.jpg'
				}
			]
		}
	},
}
</script>

<style scoped>

	.main-about {
		display: flex;
		align-items: center;
		margin: auto;
	}
</style>