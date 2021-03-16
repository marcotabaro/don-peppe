<template>
  <footer>
        <div class="contacts flex-center">
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
        <img src="img/footer-img-1.jpg" alt="Footer image">
    </footer>
</template>

<script>
export default {
    name:"MyFooter"
}
</script>

<style>
/* Footer */

footer {
    height: 400px;
    display: flex;
}

footer img {
    height: 400px;
    width: 50%;
}

.contacts {
    width: 50%;
    background-color: #1b1b1b;
}

.contacts ul li,
.working-hours li {
    display: block;
    margin: 20px 0;
    color: #767676;
    font-size: .7rem;
}


.contacts ul li span{
    display: block;
}

.footer-title {
    width: 200px;
    justify-self: flex-start;
}
</style>