<template>
  <div id="app">
    <MyHeader>
      <slider slot="slider">
      </slider>
    </MyHeader>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import slider from './components/Slider.vue'
import MyMain from './components/Main.vue'
import MyFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    slider,
    MyMain,
    MyFooter,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');

#app {
  font-family: 'Oswald', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
