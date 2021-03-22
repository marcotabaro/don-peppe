<template>
  <footer>
        <div class="contacts">
            <div class="footer-left">
                <h4>FIND OUR RESTAURANTS</h4>
            <ul>
                <li v-for="restaurant, index in restaurants" :key="index">
                    <span>{{ restaurant.address }}</span>
                    <span>{{ restaurant.country }}</span>
                    <span>{{ restaurant.number }}</span>
                </li>
            </ul>
            </div>
            <div class="footer-right">
                <h4>WORKING HOURS</h4>
                <ul class='working-hours'>
                    <li v-for="day, index in opensAt" :key="index">
                        <span>{{ day.day }}</span>
                        <span>{{ day.hours }}</span>
                    </li>
                </ul>
            </div>
                <div>
                    <h4 class='footer-title'>THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.</h4>
                </div>
        </div>
        <div class="footer-img"></div>
    </footer>
</template>

<script>
export default {
    name:"MyFooter",
    data() {
        return {
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
        }
    }
}
</script>

<style>
/* Footer */

footer {
    height: 400px;
    display: flex;
}

.footer-img {
    height: 400px;
    width: 50%;
    background-image: url("../../public/img/footer-img-1.jpg");
    background-size: cover;
    background-position: center;
}


.contacts {
    width: 50%;
    background-color: #1b1b1b;
    padding-top: 100px;
    display: flex;
    text-align:left;
}

.contacts ul li,
.working-hours li {
    display: block;
    margin: 20px 0;
    color: #767676;
    font-size: .7rem;
}

.footer-left {
    margin:0 30px;
}

.footer-right {
    margin-right: 50px;
}


.contacts ul li span{
    display: block;
}

.contacts .footer-left h4,
.contacts .footer-right h4 {
    color: #B7903C;
}


.footer-title {
    width: 195px;
    color:white;
}


</style>