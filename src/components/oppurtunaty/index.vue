<template>
    <section id="oppurtanity">
        <Container>
            <div class="wrapper" >
                <div class="title">
                    <h1>Imkoniyatlar</h1>
                    <div class="text">
                        <p>Dasturda xotin-qizlar uchun maxsus ishlab chiqilgan biznesni boshqarish, marketing va
                            sotuvlar, IT va dasturlash asoslari, hunarmandchilik, qo‘l mehnati kabi ko‘plab sohalar
                            qamrab olingan.</p>
                    </div>
                </div>
                <div class="cards">
                    <div class="line">
                        <div class="card-1">
                            <img src="../../../public/img/first.svg" alt="">
                            <p>Tadbirkorlikga oid bilimlarni o’qish imkoniyati</p>
                        </div>
                        <div class="card-1">
                            <img src="../../../public/img/second.svg" alt="">
                            <p>BMT ning maxsus kursida o‘z bilim va ko‘nimkalarini sayqallash</p>
                        </div>
                    </div>
                    <div class="line-2">
                        <div class="card-1">
                            <img src="../../../public/img/second.svg" alt="">
                            <p>O‘z bilimlaringizni test sinovlari bilan tekshirish</p>
                        </div>
                        <div class="card-1">
                            <img src="../../../public/img/third.svg" alt="">
                            <p>Imtiyozli kreditni ortiqcha ovoragarchiliklarsiz olish</p>
                        </div>
                    </div>
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section {
    font-family: Arial, Helvetica, sans-serif;
    padding: 120px 0 0 0;
    background-color: #F9F9FB;
}
.title{
    margin-bottom: 50px;
}
.title>h1 {
    font-size: 36px;
    margin-bottom: 10px;
}

.text>p {
    font-size: 18px;
    width: 1350px;
}
.cards{
    border-bottom: 1px solid #e0e5f2;
    padding-bottom: 50px;
}
.card-1{
    background-color: white;
    width: 670px;
    padding: 24px;
    border-radius: 24px;
    display: flex;
    align-items: center;
    gap: 16px;
}
.line{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.line-2{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 20px;
}
@media (max-width:1420px){
    .container{
        width: 100%;
        max-width: 992px;
        padding: 0 15px;
    }
    .card-1{
        width: 473px;
        height: 92px;
    }
}
@media (max-width:992px){
    .wrapper{
        padding: 0 40px;
    }
    .line{
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
    .line-2{
        display: flex;
        gap: 20px;
        flex-direction: column;
    }
    .card-1{
        width: 100%;
    }
    .text > p{
        width: 100%;
    }
}
@media (max-width:768px){
    .card-1{
        overflow: hidden;
    }
    .line{
        gap: 10px;
    }
    .line-2{
        gap: 10px;
    }
}
@media (max-width:400px){
    .card-1 > img{
        width: 80%;
        height: 80%;
    }
    .card-1 > p{
        font-size: 12px;
        width: 350px;
    }
}
</style>

<script setup>
import Container from "../layout/index.vue"
</script>