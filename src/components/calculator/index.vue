
<template>
    <section id="calculator">
        <Container>
            <div class="title">
                <h1>Kredit kalkulyator</h1>
            </div>
            <div class="first-body">
                <div class="text">
                    <p>Kredit kalkulyator</p>
                    <h3>Kreditlarni hisoblang</h3>
                </div>
                <button>
                    Hisoblash
                </button>
            </div>
            <div class="second-body">

                <div class="counter">
                    <p class="counter-p">
                        Boshlang'ich To'lov
                    </p>
                    <input 
                    class="range"
                        type="range" 
                        min="1000" 
                        max="1500000000" 
                        v-model="initialPayment" 
                    />
                    <div class="counter-p">
                        <p>£1000</p>
                        <p>£20k</p>
                    </div>
                    <h1>{{ formatNumber(initialPayment) }}</h1>
                </div>
                <div class="counter">
                    <p class="counter-p">
                        Boshlang'ich To'lov
                    </p>
                    <input 
                    class="range"
                        type="range" 
                        min="1" 
                        max="84" 
                        v-model="months" 
                    />
                    <div class="counter-p">
                        <p>£1000</p>
                        <p>£20k</p>
                    </div>
                    <h1>{{ months }}</h1>
                </div>


                <div class="counter">
                    <p class="counter-p">
                        Boshlang'ich To'lov
                    </p>
                        <input 
                        class="range"
                        type="range" 
                        min="1" 
                        max="24" 
                        v-model="annualRate1" 
                        />
                    <div class="counter-p">
                        <p>£1000</p>
                        <p>£20k</p>
                    </div>
                    <h1>{{ annualRate1 }}</h1>
                </div>

                <div class="counter last">
                    <p class="counter-p">
                        Boshlang'ich To'lov
                    </p>
                        <input 
                        class="range"
                        type="range" 
                        min="1" 
                        max="24" 
                        v-model="annualRate2" 
                        />
                    <div class="counter-p">
                        <p>£1000</p>
                        <p>£20k</p>
                    </div>
                    <h1>{{ annualRate2 }}</h1>
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section {

    background-color: #000000;
    color: white;
    padding-top: 50px;
}
.title {
    margin-bottom: 70px;
}
.title > h1 {
    display: flex;
    justify-content: center;
    font-size: 40px;
    font-weight: 600;
}
.first-body {
    display: flex;
    justify-content: space-between;
    align-items: end;
    margin-bottom: 80px;
}
.text > p {
    color: #72C420;
    margin-bottom: 16px;
}
.text > h3 {
    font-size: 36px;
    font-weight: 500;
    margin-bottom: 8px;
}
.text > h4 {
    font-size: 32px;
    font-weight: 500;
    opacity: 0.5;
}
.first-body > button {
    width: 159px;
    height: 56px;
    background-color: #72C420;
    border-radius: 48px;
    border: none;
    color: white;
    font-size: 16px;
    font-weight: 500;
}
.counter {
    width: 410px;
    padding-bottom: 121px;
}
.counter-p {
    margin-bottom: 14px;
    color: #808080;
    font-size: 14px;
    display: flex;
    justify-content: space-between;
}
.counter > input {
    width: 100%;
    accent-color: #72C420;
}
.counter > h1 {
    font-size: 36px;
    font-weight: 500;
}
.second-body {
    display: flex;
    gap: 40px;
    justify-content: space-between;
}
@media (max-width:1420px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }
    .second-body{
        flex-wrap: wrap;
    }
    .counter{
        width: 450px;
    }
}
@media (max-width:992px){
    .first-body{
        padding: 0 40px;
    }
    .second-body{
        padding: 0 40px;
    }
    .counter{
        width: 40%;
        padding:0;
    }
    .last{
        margin-bottom:70px;
    }
    .title >h1{
        display: none;
    }
}

@media (max-width:576px){
    .second-body{
        flex-direction: column;
        gap: 50px;
    }
    .counter{
        padding: 0px;
        width: 100%;
    }
    .first-body{
        flex-direction: column;
        align-items: start;
        gap: 20px;
    }
    .first-body > button{
        width: 108px;
        height: 40px;
    }
    .last{
        margin-bottom: 100px;
    }
    .title > h1{
        display: none;
    }
}
</style>

<script setup>
import Container from "../layout/index.vue";
import { ref } from "vue";


const initialPayment = ref(1000); 
const months = ref(1); 
const annualRate1 = ref(1);  
const annualRate2 = ref(1);  


const formatNumber = (value) => {
    return value.toString().replace(/\B(?=(\d{3})+(?!\d))/g, " ");
};
</script>