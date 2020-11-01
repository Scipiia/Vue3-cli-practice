<template>
  <div class="about">
    <h1>Галерея</h1>
    <MainAbout/>
  </div>
</template>

<script>
import MainAbout from '../components/MainAboutt'

export default {
  name: 'About',
  components: {
    MainAbout
  }
}
</script>

<style scoped>

  h1 {
    text-align: center;
  }

</style>