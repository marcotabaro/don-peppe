<template>
  <hooper :infiniteScroll="true" :autoPlay="true" :playSpeed="2500" :wheelControl="false" :centerMode="true">
    <slide v-for="(slice, index) in slicer" :key="index" :index="index" class="slide">
        <img class="resize" :src="'./img/' + slice.bg + '.png' " alt="background">
        <img class="resize" :src="'./img/' + slice.pic + '.png'" alt="slice">
    </slide>
    <hooper-navigation class="arrows-nav" slot="hooper-addons">
    </hooper-navigation>
  </hooper>
</template>

<script>
import { Hooper,
Slide,
Navigation as HooperNavigation } from 'hooper';
import 'hooper/dist/hooper.css';

export default {
  name: 'App',
  components: {
    Hooper,
    Slide,
    HooperNavigation
  },
  data() {
    return {
      slicer: [
            {
                bg: 'h3-rev-img-1', pic: 'h3-rev-img-2'
            },
            {
                bg: 'h3-rev-img-3', pic: 'h3-rev-img-4'
            },
            {
                bg: 'h3-rev-img-5', pic: 'h3-rev-img-6'
            }
        ]
    };
  }
};
</script>

<style>

.hooper {
  width: 100%;
  height: 60%;
}

.hooper:focus {
  outline: none;
}

.slide {
  align-items: center;
  display: flex;
  justify-content: center;
  margin: auto;
  position: relative;
}

.slide img {
  position: absolute;
  left: 50%;
   top: 50%;
   transform: translate(-50%,-50%);


}
.resize {
width: 250px;
height : auto;
}

.resize {
width: auto;
height : 250px;
}

.arrow-nav {
  width: 100px;
}

</style>