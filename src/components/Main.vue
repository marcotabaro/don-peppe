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
            <div class="button prev-btn flex-center">
                <a href="#">PREV</a>
            </div>
            <i class="fas fa-quote-left"></i>
            <div class='quote'>
                <span>"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</span>
            </div>
            <div class='source'>
                <span>WASHINGTON POST 2018</span>
            </div>
            <div class='mydots flex-center'>
                <i v-for="dot, index in dots" :key="index" class="fas fa-circle"></i>
            </div>
            <div class="button next-btn flex-center">
                <a href="#">NEXT</a>
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
        <div class="goahead">
            <div class="left">
                <div class="first"></div>
                <div class="second"></div>
                <div class="third"></div>
            </div>
            <div class="center">
                <div class="first"></div>
                <div class="second"></div>
                <div class="third"></div>
            </div>
            <div class="right">
                <div class="first"></div>
                <div class="second"></div>
                <div class="third"></div>
            </div>
        </div>

        <div class="team">
            <ul>
                <li v-for='worker, index in team' :key="index">
                    <img :src="'img/' + worker.pic + '.jpg'" alt="Staff Images">
                </li>
            </ul>
        </div>

        <div class="clients flex-center">
            <ul class='flex-center'>
                <li class='flex-center' v-for='client, index in clients' :key="index">
                    <img :src="'img/' + client + '.png'" alt="Logo clients">
                </li>
            </ul>
        </div>

        <div class="pizza-slider flex-center">
            <div class="header flex-center">
                <h5>CHOOSE YOUR FLAVOR</h5>
                <h2>THE BEST PIZZA MENU IN TOWN</h2>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt et, nisi reprehenderit cumque maiores minus officia accusantium mollitia ut ad ea alias.</p>
            </div>
            <div class='slider-bot'>
                <ul class='flex-center'>
                    <li class='flex-center' v-for="pizza, index in pizzas" :key="index">
                        <img :src="'img/' + pizza.pic + '.png'" alt="pizza pictures">
                        <p class='name'>{{ pizza.name }}</p>
                        <p class='price'>{{ pizza.price }}</p>
                    </li>
                </ul>
            </div>
        </div>

        <div class="deals">
            <div class=details>
                <div class="events">
                    <div class='title'>
                        <p>MADE WITH LOVE</p>
                        <h2>DELISH PIZZA DEALS</h2>
                    </div>
                    <div class="place">
                        <div class="date">
                            <h1>02</h1><h4>NOV</h4>
                        </div>
                        <div class="location">
                            <h4>TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO</h4>
                            <p><i class="fas fa-map-marker-alt"></i> 204 E.Piazzetta Tommaso</p>
                        </div>
                    </div>
                    <div class="place">
                        <div class="date">
                            <h1>03</h1><h4>NOV</h4>
                        </div>
                        <div class="location">
                            <h4>TERRAZZA PATIO DINING SPACE OPENING THIS WEEKEND</h4>
                            <p><i class="fas fa-map-marker-alt"></i> 204 E.Piazzetta Tommaso</p>
                        </div>
                    </div>
                    <div class="place">
                        <div class="date">
                            <h1>05</h1><h4>NOV</h4>
                        </div>
                        <div class="location">
                            <h4>SIENNA PRIVATE DINING ROOM WITH STEPHANE BRUNN</h4>
                            <p><i class="fas fa-map-marker-alt"></i> 204 E.Piazzetta Tommaso</p>
                        </div>
                    </div>
                </div>
            </div>
            <img src="img/h3-img-5a.jpg" alt="cartoon">
        </div>
        <div class="booking flex-center">
            <input type="text" placeholder="1 Person">
            <span>FOR</span>
            <input type="text" placeholder="11/29/2020">
            <span>AT</span>
            <input type="text" placeholder="7:00 pm">
            <button>BOOK A TABLE</button>
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
            images: ['h3-img-1', 'h3-img-2', 'h3-img-3', 'h3-img-4'],
            dots: 3,
        team: [
            {
                name: 'Jack Skeleton', pic: 'h1-team-1a-700x700', role: 'Cook Master',
            },
            {
                name: 'Frank Bailey', pic: 'h1-team-2a', role: 'Kitchen Porter',
            },
            {
                name: 'Karen Ross', pic: 'h1-team-3a', role: 'Kitchen Porter',
            },
            {
                name: 'Jhon Jhonson', pic: 'h1-team-4a', role: 'Delivery Guy',
            }
        ],
        clients: ['h1-clients-img-4', 'h1-clients-img-3', 'h1-clients-img-1', 'h1-clients-img-2', 'h1-clients-img-5'],
        pizzas: [
            {
                name: 'BISMARCK', pic: 'h3-product-img-1a-100x100', price: '$5.00 - $30.00'
            },
            {
                name: 'FIORI DI ZUCCA', pic: 'h3-product-img-2a-150x150', price: '$7.00 - $50.00'
            },
            {
                name: 'VALDOSTANA', pic: 'h3-product-img-3a-150x150', price: '$55.00'
            },
            {
                name: 'PIZZA TARTUFATA', pic: 'h3-product-img-4a-150x150', price: '$45.00'
            },
            {
                name: 'FRANCESCANA', pic: 'h3-product-img-5a-150x150', price: '$25.00'
            },
            {
                name: 'CAMPAGNOLA', pic: 'h3-product-img-6a-100x100', price: '$50.00 - $95.00'
            }
        ],
        restaurants: [
            {
                address: '1614 E. Bell Rd #104.', country:'Salerno, AZ 85022', number: '(602) 867-1010'
            },
            {
                address: '204 E. Piazzetta Tommaso', country:'Sorrento, AZ 85022', number: '(358) 867-1010'
            },
            {
                address: 'Viale Puglia 54', country:'Torre Del Greco AZ 85022', number: '(359) 867-1010'
            },
            {
                address: 'Corso Italia AA', country:'Naples, AZ 85022', number: '(989) 867-1010'
            }
        ],
        opensAt: [
            {
                day: 'MONDAY', hours: 'Kitchen Closed'
            },
            {
                day: 'TUESDAY UNTIL FRIDAY', hours: '9:00 - 22:00'
            },
            {
                day: "SATURDAY", hours: 'Saturday 11am to midnight'
            },
            {
                day: 'SUNDAY', hours:'9:00 - 22:00'
            }
        ]
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
    background-position: center;
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

.button {
    background-color: white;
    width:60px;
    height:25px;
    border-top-left-radius:25px;
    border-top-right-radius:25px;
    font-size:.6rem;
    color: #d65739;
}

.prev-btn {
    position:absolute;
    left:-15px;
    transform: rotate(90deg);
}

.next-btn {
    position:absolute;
    right:-15px;
    transform: rotate(-90deg);
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
    background-size: 100% 500px;
    background-position: bottom;
}

.goahead .center .second {
    height: 50%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-size: 100% 550px;
}

.goahead .center .third {
    height: 25%;
    background-image: url(../../public/img/h3-background-img.jpg);
    background-size: 100% 700px;
    background-position: center;
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

/* Team */

.team ul li {
    width: 25%;
    padding: 5px 0;
}

.team ul li img {
    height: 335px;
    width: 100%;
}

/* Clients */
.clients {
    background-color: #f7f7f2;
}

.clients ul {
    width: 80%;
    flex: 0 0 5;
}

.clients ul li {
    margin: 40px 0px;
    width: 15%;
    height: 20%;
}

.clients ul li img {
    width: 90%;
    height: 90%;
}


/* Pizza Slider */

.pizza-slider {
    height: 550px;
    flex-flow: column nowrap;
    overflow-x: hidden;
}

.pizza-slider .header {
    flex-flow: column nowrap;
    width: 40%;
    margin-bottom: 50px;
}

.pizza-slider .header p {
    text-align: center;
    color: #B2B2B2;
    font-size: .8rem;
}

.pizza-slider .header h5 {
    color: #D2401E
}

.pizza-slider .header h2 {
    margin: 15px 0;
}

.slider-bot ul li img{
    width: 150px;
    margin: 15px 50px;
}

.slider-bot ul li {
    flex-flow: column nowrap;
}

.slider-bot .name {
    color: #B68A2B;
    font-size: .8rem;
    margin-bottom: 5px;
    font-weight: bold;
}

.slider-bot .price {
    color: #D23F1D;
    font-size: .7rem;
    font-weight: bold;
}

/* DEALS */

.deals {
    height: 550px;
    display: flex;
    color: white;
    font-size: .8rem;
}

.deals .details .events {
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
}

.deals .events .title {
    left: -80px;
    position: relative;
}
.deals .events p{
    color: #AB4027;
    margin-top: 30px;
}
.deals .events h2 {
    margin: 15px 0 35px 0;
}

.deals .details {
    width: 50%;
    height: 500px;
    background-color: #1C1C1C;
}

.deals img {
    width: 50%;
    height: 550px;
}

.deals .details .place {
    display: flex;
    align-items: center;
    border-bottom: #B68A2B dotted 2px;
    width: 350px;
}

.deals .details .place:last-child {
    border-bottom: none;
}

.location {
    display: flex;
    flex-flow: column nowrap;
    align-items: flex-start;
    justify-content: center;
}

.location h4 {
    margin-top: 20px;
}

.deals .details .date {
    margin-right: 20px;
    margin-bottom: 50px;
}

.deals .details .date h1 {
    color: #AB4027;
    font-size: 2rem;
    font-weight: bolder;
}

.deals .details .events .location p {
    margin: 10px 0 50px 0;
}

/* Booking */

.booking {
    height: 150px;
    background-image: url(../../public/img/h3-background-img-3.jpg);
    background-size: cover;
    color: white;
    margin-bottom: 5px;
}

.booking input {
    padding: 10px;
    margin:0 15px 0 15px;
    border: 1px solid black;
}

.booking button {
    padding: 15px 35px;
    color: white;
    background-color: #D2401E;
    border: none;
    font-size: .6rem;
}

</style>