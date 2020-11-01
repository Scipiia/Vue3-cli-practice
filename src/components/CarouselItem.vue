<template>
	<div class="carousel-item">
		<img v-bind:src="require('../assets/ImageAbout/' + item_data.image)" alt="" v-if="imageSlide">
		<div class="item__content" v-else>
			<p>{{item_data.name}}</p>
			<p>{{item_data.id}}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'carousel-item',
	props: {
		item_data: {
			type: Object,
			default: () => {}
		},
		imageSlide: {
			type: Boolean,
			default: true
		}
	}
}
</script>

<style scoped>

	img {
		width: 800px;
		height: 600px;
	}

	.item__content{
		width: 800px;
	}
</style>