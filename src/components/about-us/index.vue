<template>
    <section   ref="aboutUsSection">
        <Container>
            <div class="wrapper" >
                <div class="content">
                    <p>Dastur haqida</p>
                    <h3>Mazkur loyiha O‘zbekiston Respublikasi Prezidentining PQ-385 qaroriga <span> asosan mamlakatimizdagi xotin-qizlarni tadbirkorlikka o‘qitish, moliyaviy yordam ko‘rsatish, shuningdek, ulardagi tadbirkorlik ko’nikmalarini rivojlantirishga qaratilgan. </span> </h3>

                </div>
                <div class="banner">
                    <img src="../../../public/img/group.svg" alt="">
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
    .wrapper{
        display: flex;
        padding: 70px 0 ;
        gap: 80px;
    }
    p{
    font-family: italic;
    color: #72C420;
    font-size: 18px;
    font-weight: 400;
    transform: skewX(-10deg); 
    margin-bottom: 10px;
    }
    img{
        width: 495px;
        height: 320px;
    }
    h3{
        font-family: Arial, Helvetica, sans-serif;
        color: white;
        font-size: 32px;
        font-weight: 500;
        width: 670px;

    }
    section{
        background-color: #000000;
    }
    span{
        opacity: 0.5;

    }
    @media (max-width:1420px){
        .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
        }
        img{
            width: 400px;
            height: 259px;
        }
        .content > h3{
            font-size: 24px;
            width: 450px;
            line-height: 125%;
            font-weight: 500;
        }
    }
    @media (max-width:992px){
        .wrapper{
            flex-direction: column;
            align-items: center;
        }
        .content{
            width: 700px;
        }
        .content > h3{
            width: 700px;
        }
        .banner > img{
            width:  1000px;
            height: 450px;
        }
    }
    @media (max-width:768px){
        .wrapper{
            margin: 0 40px;
        }
        .content >h3{
            position: absolute;
            max-width: 80%;
            font-size: 24px;
            left: 50px;
            margin-top: 50px;
        }
        .content > p{
            padding: 0 30px;
            position: absolute;
            left: 20px;
        }
        img{
            margin-top: 120px;
            max-width: 90%;
        }
    }
    @media (max-width:576px){
        img{
            margin-top: 150px;
        }
    }
    @media (max-width:400px){
        .content > h3{
            font-size: 18px;
        }   
        img{
            margin-top: 50px;
            width: 100%;
        }
    }
</style>

<script setup>
import Container from "../layout/index.vue"
</script>