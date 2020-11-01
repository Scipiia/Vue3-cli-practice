<template>
	<div class="form">
		<h3 class="form-title">Вперед, играть</h3>
		<form v-on:submit.prevent="onSubmit" class="form-form">
			<strong class="form-subtitle">Зарегистрируйтесь, создаите персонажа и начните играть</strong>
			<span class="form-email">Ваш Email: {{email}}</span>
			<input type="text" placeholder="email" v-model="email">
			<button class="form-btn">Регистрация</button>
		</form>
	</div>
</template>

<script>
export default {
	name: 'form',
	data() {
		return {
			email: '',
		}
	}
}
</script>

<style scoped>
	.form {
		display: flex;
		flex-direction: column;
		align-items: center;
		background: rgba(236, 137, 137, 0.829);
		padding-bottom: 60px;
	}

	.form-form{
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.form-email {
		font-size: 20px;
		margin-top: 40px;
	}

	.form-title {
		font-size: 26px;
	}

	.form-subtitle {
		font-size: 22px;
	}

	.form-btn {
		margin-top: 10px;
	}

</style>