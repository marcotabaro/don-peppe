<template>
    <main>
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
        <div class="slider flex-center">
            <i class="fas fa-quote-left"></i>
            <div class='quote'>
                <span>"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</span>
            </div>
            <div class='source'>
                <span>WASHINGTON POST 2018</span>
            </div>
            <div class='mydots flex-center'>
                <!-- <i v-for="dot in dots" class="fas fa-circle"></i> -->
            </div>
        </div>

        <div class="menu">
            <img src="img/h1-img-4.jpg" alt="pizza Specials">
            <div class="wrapper flex-center">
                <div class="specials">
                    <h2>SPECIALS*</h2>
                    <span>lorem ipsum dolor sit amet, consectetur adipiscing elit.Praesent ut.</span>
                    <ul>
                        <li class='title-list'><h4>$10 COMBO PICCOLO</h4></li>
                        <li>lorem ipsum dolor sit amet, consectetur adipiscing elit.Praesent ut.</li>
                        
                        <li class='title-list'><h4>$20 COMBO MEZZO</h4></li>
                        <li>lorem ipsum dolor sit amet, consectetur adipiscing elit.Praesent ut.</li>
    
                        <li class='title-list'><h4>$30 COMBO GRANDE</h4></li>
                        <li>lorem ipsum dolor sit amet, consectetur adipiscing elit.Praesent ut.</li>
                    </ul>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: "MyMain",
    components: {

    },
    data() {
        return {
            images: ['h3-img-1', 'h3-img-2', 'h3-img-3', 'h3-img-4']
        };
    },
};
</script>

<style>

/* slider */

.slider {
    height: 300px;
    background-image: url(../../public/img/h3-testimonials-bckgrnd.jpg);
    background-size: cover;
    flex-flow: column nowrap;
}

.slider .fa-quote-left {
    font-size: 3rem;
    color: #b7903c;
    margin-bottom: 20px;
}

.quote {
    width: 500px;
    text-align: center;
}
.source{
    color: #d65739;
    margin: 20px 0;
}

.source span {
    font-size: .6rem;
}

.mydots .fas {
    margin-left: 5px;
    font-size: .6rem;
    color: lightgrey;
}

/* MENU SECTION */
.menu {
    height: 550px;
    display: flex;
}

.wrapper {
    width: 100%;
    height:100%;
    flex-flow: column nowrap;
}

.menu img {
    height: 100%;
    width: 50%;
    padding: 5px 0;
}

.specials {
    display: flex;
    flex-flow: column nowrap;
    height: 60%;
    width: 50%;
}
.menu .wrapper .specials li {
    display: block;
    margin: 15px 0;
}

.specials span,
.specials ul li:nth-child(even) {
    color: #B2B2B2;
    font-size: .8rem;
}

.goahead {
    height: 350px;
    display: flex;
    flex-flow: row nowrap;
}

.left {
    width: 7%;
    background-image: url(../../public/img/h3-background-img.jpg);
}

.center {
    width: 86%;
}

.right {
    width: 7%;
    background-image: url(../../public/img/h3-background-img.jpg);
}

.goahead .center .first {
    height: 25%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-size: cover;
    background-position: bottom;
}

.goahead .center .second {
    height: 50%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-size: cover;
    background-position-y: 200vh;
}

.goahead .center .third {
    height: 25%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-size: cover;
    background-position-y: 50vh;
}

.goahead .left .first,
.goahead .left .third {
    height: 25%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-position: bottom;
}

.goahead .right .first,
.goahead .right .third {
    height: 25%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-position-y: 50vh;
}

.goahead .left .second,
.goahead .right .second {
    height: 50%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-position: center;
}

</style>