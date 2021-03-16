<template>
  <header>
    <nav>
      <button>ORDER ONLINE</button>

      <!-- generated with Vue -->
      <div class="link">
        <ul>
          <li v-for="(link, index) in links[0]" :key="index">
            <a href="#"> {{ link }} </a>
          </li>
        </ul>
        <img src="../../public/img/h5-logo-divided-header.png" alt="Don Peppe Logo"/>
        <ul>
          <li v-for="(link, index) in links[1]" :key="index">
            <a href="#">{{ link }}</a>
          </li>
        </ul>
      </div>
      <div class="right-nav flex-center">
        <a class="flex-center" href="#">
          <img src="../../public/svg/svg-1.svg" alt="scooter" />
          <span>CART</span>
        </a>
        <a href="#">
          <i class="fas fa-search"></i>
          <span>SEARCH</span>
        </a>
      </div>
    </nav>

    <!-- slice + slider =  -->
    <slider class="hooper"/>
    <div class="header-bot">
      <ul class='flex-center'>
        <li v-for='(image, index) in images' :key="index">
          <div class="flip-card">
            <div class="flip-card-inner flex-center">
              <div class="img1">
                <img :src="'img/' + image + '.jpg'" alt="Header Images">
              </div>
              <div class="img2 flex-center">
                <i class="fas fa-eye fa-2x flex-center"></i>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </header>
</template>
<script>

import slider from "./slider.vue";
export default {
  name: "MyHeader",
  components: {
    slider
  },
  data() {
    return {
      hovering: "",
      isHovering: false,
      links: [
        ["HOME", "PAGES", "MENU"],
        ["EVENT", "BLOG", "LANDING"],
      ],
      images: ['h3-img-1', 'h3-img-2', 'h3-img-3', 'h3-img-4']
    };
  },
};
</script>

<style>

/* HELPER */

.flex-center {
    display: flex;
    justify-content: center;
    align-items: center;
}



* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
}

a {
    text-decoration: none;
    color: inherit;
}

li {
     display: inline-block;
 }

ul {
     list-style-type: none;
 }

body {    
    margin: 0 !important;
    padding: 0 !important;
    overflow-x: hidden;
}
#app {
  margin-top: 0px !important;
}

header {
    background-color: #181818;
    height: 450px;
}

header nav {
    font-size: 0.7rem;
    margin: 0 auto;
    width: 1000px;
    height:100px;
    color: white;
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 30px;

}

header nav button {
    padding: 15px 25px;
    color: white;
    background-color: #D2401E;
    border: none;
    font-size: .6rem;
}

header nav .link {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
}

header nav .link ul {
    list-style-type: none;
}

header nav .link ul li {
    display: inline-block;
    margin: 0 15px;
}


header nav .link img {
    width: 150px;
    height: 100px;
    margin-top: 20px;
}

.right-nav a img{
    filter: invert(100%);
    margin-right: 20px;
}

.right-nav a:first-of-type {
    margin-right:20px;
}


.header-bot {
  margin-top: 55px;
}

.header-bot ul li {
  width: 25%;
}

.header-bot ul li img {
    height:100%;
    width: 100%;
    padding: 5px 5px 5px 5px;
}


.flip-card {
  background-color: transparent;
  height: 250px;
  perspective: 800px;
  cursor:pointer;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.img1 {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}


.img2 {
  width:100%;
  height:100%;
  transform: rotateY(180deg);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAIAAAACCAYAAABytg0kAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAABZJREFUeNpi2r9//38gYGAEESAAEGAAasgJOgzOKCoAAAAASUVORK5CYII=);
}

.fa-eye {
  background-color:#d2401e;
  color: white;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
</style>