<template>
    <div class="wrapper">
        <Container>
            <div class="nav">
                <div class="logo">
                    <a href="#"><img src="../../../public/img/logo.svg" alt=""></a>
                </div>
                <ul class="menu" style="cursor: pointer;" :class="{ 'menu--open': isMenuOpen }">
                    <li><a @click.prevent="scrollToSection('aboutus')">Dastur haqida</a></li>
                    <li><a @click.prevent="scrollToSection('oppurtanity')">Imkoniyatlar</a></li>
                    <li><a @click.prevent="scrollToSection('forwho')">Ishtirokchilar</a></li>
                    <li><a @click.prevent="scrollToSection('steps')">Bosqichlar</a></li>
                    <li><a @click.prevent="scrollToSection('calculator')">Kredit Kalkulyator</a></li>
                </ul>
                <div class="menu-2">
                    <li>Hamroh haqida</li>
                    <li>Imkoniyatlar</li>
                    <li>Kimlarga tegishli</li>
                    <li>Bosqichlar</li>
                    <li>Kredit kalkulyator</li>

                </div>

                <div class="login">
                    <p>Tizimga kirish</p>
                    <img src="../../../public/img/login.svg" alt="">
                </div>

                <div class="burger" :class="{ open: isMenuOpen }" @click="toggleMenu">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
        </Container>
    </div>
    <section class="second">
        <Container>
            <div class="image-wrapper">
                <div class="wrap">
                    <div class="text">
                        <h1>Ayollar tadbirkorligini
                            qo‘llab-quvvatlash dasturi</h1>
                        <p>
                            Dastur orqali ta‘lim oling
                            va imtiyozli kreditga ega bo‘ling!
                        </p>
                        <div class="button">
                            <button>Tizimga kirish</button>
                        </div>
                    </div>
                </div>
                <div class="left-image">
                    <img class="women" src="../../../public/img/women.svg" alt="">
                    <img class="girl" src="../../../public/img/girl.svg" alt="">
                </div>
                <img class="women-2" src="../../../public/img/women2.svg" alt="">
                <img class="half-girl" src="../../../public/img/half-girl.svg" alt="">
                <div class="right">
                    <img class="half-women" src="../../../public/img/half-women.svg" alt="">
                    <img class="girl-flower" src="../../../public/img/girl-flower.svg" alt="">
                </div>
                <img class="girl-comp" src="../../../public/img/girl-comp.svg" alt="">
            </div>
        </Container>
    </section>
</template>



<script setup>
import { ref, onMounted } from "vue";
import Container from "../layout/index.vue";



const isMenuOpen = ref(false);
const isSmallScreen = ref(false);

const closeMenu = () => {
    isMenuOpen.value = false;
};

const scrollToSection = (id) => {
    const section = document.getElementById(id);
    if (section) {
        section.scrollIntoView({ behavior: "smooth" });
    }
    closeMenu();
};


const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};




</script>

<style scoped>
.wrapper {
    background-color: #f2f8d8;
    border-bottom: 1px solid #e0e0e2;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    width: 100%;
    z-index: 100;
}



.nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 70px;
}

.logo>a {
    color: black;
    text-decoration: none;
}

.menu {
    font-family: HelveticaMain, sans-serif;
    list-style: none;
    display: flex;
    align-items: center;
    gap: 40px;
    justify-content: space-between;
}

.menu-2 {
    display: none;
}

.burger {
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 32px;
    height: 24px;
    overflow: hidden;
    cursor: pointer;
    position: fixed;
    top: 20px;
    right: 20px;
    z-index: 1000;
}

.burger span {
    width: 100%;
    height: 4px;
    background-color: #3d3d3d;
    border-radius: 2px;
    transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
    position: absolute;
}


.burger span:nth-child(1) {
    top: 0;
}

.burger span:nth-child(2) {
    top: 10px;
}

.burger span:nth-child(3) {
    top: 20px;
}


.burger.open span:nth-child(1) {
    transform: rotate(45deg) translate(7px, 7px);
}

.burger.open span:nth-child(2) {
    opacity: 0;
}

.burger.open span:nth-child(3) {
    transform: rotate(-45deg) translate(7px, -7px);
}


li>a {
    color: black;
    text-decoration: none;
}

li>a:hover {
    color: #656569;
}

.login {
    display: flex;
    gap: 10px;
    cursor: pointer;
}

.second {
    position: relative;
    background-color: #f2f8d8;
    padding-top: 80px;
    overflow: hidden;
    height: 100%;

    margin: -20px auto;
    /* background-color: red; */
}

.image-wrapper {
    position: relative;
    width: 1400px;
}

.women {
    position: absolute;
    top: 70px;
}

.girl {
    position: absolute;
    top: 250px;
    left: 7%;
}

.women-2 {
    position: absolute;
    top: 500px;
    left: 5%;
}

.half-girl {
    position: absolute;
    bottom: 0;
    left: 25%;
}

.half-women {
    position: absolute;
    top: 0;
    right: 250px;
}

.girl-flower {
    position: absolute;
    bottom: 300px;
    right: 50px;
}

.girl-comp {
    position: absolute;
    bottom: 0;
    right: 250px;
}

.wrap {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 700px;
    font-family: Arial, Helvetica, sans-serif;
}

.text {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.text>h1 {
    text-align: center;
    font-size: 64px;
    width: 800px;
    margin-bottom: 10px;
}

.text>p {
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    width: 250px;
    text-align: center;
    margin-bottom: 20px;
}

button {
    background-color: #72c420;
    border: none;
    border-radius: 48px;
    color: white;
    font-weight: 600;
    padding: 16px 40px;
}

.login>p {
    font-size: 16px;
    font-family: Arial, Helvetica, sans-serif;
}

@media (max-width:1420px) {
    .container {
        width: 100%;
        max-width: 992px;
    }

    .women {
        width: 140px;
        height: 168px;
    }

    .girl {
        width: 100px;
        height: 67px;
        top: 27%;
    }

    .women-2 {
        width: 146px;
        height: 176px;
    }

    .half-girl {
        left: 250px;
        width: 239px;
        height: 165px;
    }

    .girl-comp {
        width: 147px;
        height: 167px;
        /* bottom: 100px; */
        right: 100px;
    }

    .girl-flower {
        width: 170px;
        height: 162px;
        right: 0;
    }

    .half-women {
        width: 300px;
        height: 243px;
        top: -70px;
    }

    .text>h1 {
        width: 600px;
        font-size: 48px;
        font-weight: 500;
    }

    .text>p {
        font-size: 18px;
        width: 250px;
        line-height: 140%;
    }

    .image-wrapper {
        width: 100%;
    }

}





@media (max-width:1120px) {
    .girl-flower {
        width: 170px;
        /* right: 7%; */
    }
}

@media (max-width:1060px) {
    .girl {
        left: 12%;
    }

    .women-2 {
        left: 7%;
    }



    .half-girl {
        width: 210px;
    }

    .girl-comp {
        right: 20%;
    }
}

@media (max-width: 992px) {
    .nav {
        padding: 0 40px;
    }

    .burger {
        position: absolute;
        right: 5%;
        display: flex;
    }

    .burger>span {
        display: flex;
    }

    .menu {
        display: flex;
        flex-direction: column;
        justify-content: start;
        position: fixed;
        top: 0;
        left: -100%;
        top: 71px;
        width: 100%;
        height: 100vh;
        background-color: #f2f8d8;
        padding: 20px;
        border-right: 1px solid #e0e0e2;
        transition: left 0.3s ease-in-out;
    }

    .menu.menu--open {
        left: 0px;
    }

    .menu.menu--open {
        display: flex;
    }

    .login {
        display: none;
    }

    .women {
        width: 120px;
        height: 150px;
        left: 40px;
    }

    .women-2 {
        width: 130px;
        height: 157px;
    }

    .girl {
        width: 80px;
        height: 50px;
        left: 120px;
    }

    .half-women {
        width: 230px;
        height: 186px;
        right: 150px;
    }

    .girl-flower {
        height: 130px;
        top: 150px;
        /* right: 50px; */
    }

    .girl-comp {
        right: 50px;
    }

    .text>h1 {
        width: 500px;
        font-size: 40px;
    }
}

@media (max-width:700px) {
    .girl-flower {
        width: 140px;
        height: 144px;
        top: 100px;
    }

    .women {
        width: 92px;
        height: 111px;
    }

    .girl {
        width: 72px;
        height: 48px;
        top: 150px;
        left: 80px;
    }

    .half-women {
        width: 221px;
        height: 179px;

    }

    .half-girl {
        width: 150px;
    }

    .girl-comp {
        width: 130px;
        height: 150px;
        right: 0;
    }
}

@media (max-width:576px) {
    .half-women {
        width: 116px;
        height: 94px;
        top: 0;
        right: 100px;
    }

    .girl-flower {
        width: 103px;
        height: 83px;
        right: 0;
    }

    .women {
        left: 0;
    }

    .girl {
        left: 50px;
    }

    .women-2 {
        width: 76px;
        height: 92px;
    }

    .half-girl {
        width: 110px;
        height: 132px;
        bottom: 30px;
        left: 150px;
        border-radius: 8px;
    }

    .girl-comp {
        width: 78px;
        height: 93px;
        bottom: 100px;
    }

    .text>h1 {
        width: 90%;
    }

    .text>p {
        font-size: 12px;
        width: 29%;
    }
}

@media (max-width:400px) {
    .text>h1 {
        font-size: 32px;
    }

    .text>p {
        font-size: 10px;
    }

    .nav {
        padding: 0 20px;
    }
}
</style>