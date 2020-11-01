<template>
  <div>
    <div class="hello">
      <span class="hello-subtitle">Тактический шутер 5 на 5 и уникальными персонажами</span>
      <h1 class="hello-title">VALORANT</h1>
      <button class="hello-btn">ИГРАТЬ</button>
    </div>
    <Description/>
    <Cards/>
    <Form/>
  </div>
</template>

<script>
import Description from './Description'
import Form from './Form'
import Cards from './Cards'

export default {
  name: 'Main',
  components: {
    Description,
    Form,
    Cards
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello {
    background-image: url("../assets/valorant.jpg");
    background-repeat: no-repeat;
    background-position: center;
    height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    text-align: center;
  }

  .hello-title{
    margin: 0;
    padding: 0;
    color: white;
    font-size: 60px;
    opacity: 0.6;
    margin-top: 20px;
  }

  .hello-subtitle{ 
    color: white;
    margin-top: 250px;
    opacity: 0.6;
    font-size: 22px;
  }

  .hello-btn{
    padding: 20px 70px;
    background: rgba(255, 255, 255, 0);
    font-size: 22px;
    color: white;
    margin-top: 20px;
    opacity: 0.6;
  }

  .hello-btn:hover {
    background: rgba(156, 20, 20, 1);
  }
</style>
