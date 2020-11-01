<template>
  <div id="nav">
    <router-link class="aaa" to="/">Об игре</router-link> 
    <router-link class="aaa" to="/about">Медиа</router-link>
  </div>
  <router-view/>
</template>

<style scoped>

 #nav {
    display: flex;
    justify-content: center;
    color: white;
    background: rgb(78, 75, 78);
    padding-top: 20px;
    padding-bottom: 20px;
 }

 .aaa {
   color: white;
   font-size: 22px;
   text-decoration: none;
   margin-right: 20px;
 }

</style>
