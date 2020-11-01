<template>
	<div class="description">
		<h2 class="description-title">МЫ – VALORANT</h2>
		<span class="description-subtitle">СОТРИ ГРАНИЦЫ</span>
		<p class="description-text">VALORANT – это ваша глобальная соревновательная сцена. 
			Тактический шутер с матчами 5 на 5, установкой и обезвреживанием 
			Spike и одной жизнью на раунд. Матчи ведутся до 13 побед в раундах.
			В вашем арсенале – не только оружие и патроны, но также
			разнообразные агенты, каждый из которых обладает универсальными, 
			молниеносными и смертельно опасными умениями, позволяющими вам в 
			полной мере продемонстрировать свое мастерство стрелка.
			Креативность – ваше главное оружие.
		</p>
	</div>
</template>

<script>
export default {
	name: 'description'
}
</script>

<style scoped>
	.description{
		display: flex;
		flex-direction: column;
		flex-basis: 30%;
		background: rgba(197, 189, 189, 0.829);
		background-image: url("../assets/fonst.jpg");
		background-repeat: no-repeat;
    background-position: right;
		height: 100vh;
	}

	.description-title {
		font-size: 33px;
		margin-top: 50px;
	}

	.description-subtitle{
		color: rgb(56, 50, 50);
		margin-left: 100px;
		margin-top: 50px;
	}

	.description-text{
		color: rgb(56, 50, 50);
		width: 300px;
		margin-left: 100px;
		line-height: 25px;
		margin-top: 30px;
	}
</style>