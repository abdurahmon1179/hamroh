<template>
    <section>
        <Container>
            <div class="wrapper">
                <div class="title">
                    <h1>Hamkorlarimiz</h1>
                </div>
                <div class="sponsors">
                    <div class="realsoft">
                        <img src="../../../public/img/rs-logo.svg" alt="">
                    </div>
                    <div class="xalq-bank">
                        <img src="../../../public/img/brb-logo.svg" alt="">
                    </div>
                    <div class="brb">
                        <img src="../../../public/img/xalq-logo.webp" alt="">
                    </div>
                    <div class="mkb">
                        <img src="../../../public/img/mkb-logo.svg" alt="">
                    </div>
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section{
    background-color: #f2f8d8;
}
h1{
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    padding: 120px 0 40px 0;
    font-size: 36px;
}
img{
    width: 200px;
    height: 70px;
    object-fit: contain;
}
.realsoft{
    height: 134px;
    border: 1px solid #e0e5f2;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: none;
    border-bottom-left-radius: 25px;
    border-top-left-radius: 25px;
}
.xalq-bank{
    height: 134px;
    border: 1px solid #e0e5f2;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: none;
}
.brb{
    height: 134px;
    border: 1px solid #e0e5f2;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    border-right: none;
}
.mkb{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 134px;
    width: 100%;
    border: 1px solid #e0e5f2;
    border-bottom-right-radius: 25px;
    border-top-right-radius: 25px;
}
.sponsors{
    display: flex;
    justify-content: space-between;
    padding-bottom: 120px;
}
@media (max-width:1420px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }
}
@media (max-width:992px){
    img{
        width: 60%;
        height: 30%;
    }
}
@media (max-width:576px) {
    
}
</style>

<script setup>
import Container from "../layout/index.vue"
</script>