<template>
	<div class="agents">
		<h1 class="agents-title">Агенты</h1>
		<CardsItem
			v-for="(agent, index) in agents"
      :key="agent"
      v-bind:agent_data="agent"
      @toggle="agents.splice(index, 1)"

      @flipped="seeImage"
      v-bind:flipped_card="flipped"
		/>
	</div>
</template>

<script>
import CardsItem from './Cards-item'

export default {
	name: 'Cards',
	components: {
		CardsItem
  },
   methods: {
    seeImage() {
      this.agents.isActive = !this.agents.isActive //меняю состояние и нужно передать дочернему элементу
      console.log(this.agents.isActive)           
   }
  },
  computed: {
   
  },
	data() {
    return {
      agents: [
        {
          id: 1,
          name: 'Viper',
          role: 'Expert',
          bio: 'Химик из США Viper устанавливает контроль над полем боя с помощью источающих токсичный газ устройств и ограничивает обзор противникам. А тех, кого ей не удастся отравить, она непременно перехитрит.',
					image: '1.jpeg',
					isActive: false
        },
        {
          id: 2,
          name: 'Sage',
          role: 'Guardian',
          bio: 'Защитница Китая Sage обеспечивает безопасность команды в бою. Благодаря возможности воскрешать союзников и сдерживать натиск врага она создает оазис покоя на жутком поле боя.',
          image: '2.jpeg',
          isActive: false
        },
        {
          id: 3,
          name: 'Gypher',
          role: 'Guardian',
          bio: 'Торговец информацией из Марокко Cypher может самостоятельно создать целую информационную сеть для отслеживания действий противника. Под неусыпным взором Cypher все тайное становится явным.',
          image: '3.jpeg',
          isActive: false
        },
        {
          id: 4,
          name: 'Jett',
          role: 'Duelist',
          bio: 'Представляющая Южную Корею Jett быстра и неуловима и может позволить себе рисковать чаще других. В любой стычке она заходит с флангов и быстро уничтожает растерявшегося противника.',
          image: '4.jpg',
          isActive: false
        }
      ]
    }
  }
}
</script>


<style scoped>

  .agents{
    background: dimgrey;
    padding-top: 40px;
    padding-bottom: 60px;
  }

  .agents-title {
    text-align: center;
    color: white;
    margin-bottom: 40px;
  }
</style>

