<template>
    <section id="steps">
        <Container>
            <div class="title">
                <h1>Dastur bosqichlari</h1>
                <p>Our Ecosystem consists of four major parts, which support each other thus allow to achieve synergetic
                    gain.</p>
            </div>
            <div class="text">
                <div class="box">
                    <h1>1</h1>
                    <div class="text-title">
                        <h2>Ariza berish va skoring</h2>
                        <p>Our Ecosystem consists four major parts, which support each other thus allow to achieve
                            synergetic gain.</p>
                    </div>
                </div>
            </div>

            <div class="text">
                <div class="box">
                    <h1>2</h1>
                <div class="text-title">
                    <h2>Kichik biznes va xususiy tadbirkorlik kursida o'qish</h2>
                    <p>Our Ecosystem consists four major parts, which support each other thus allow to achieve
                        synergetic gain.</p>
                </div>
                </div>
            </div>

            <div class="text">
                <div class="box">
                    <h1>3</h1>
                <div class="text-title">
                    <h2>Shaxsiy biznes rejani shakllantirish</h2>
                    <p class="none">Our Ecosystem consists four major parts, which support each other thus allow to
                        achieve
                        synergetic gain.</p>
                </div>
                </div>
            </div>

            <div class="text last">
                <div class="box">
                    <h1>4</h1>
                <div class="text-title">
                    <h2>Kredit olish uchun ariza yuborish</h2>
                    <p>Our Ecosystem consists four major parts, which support each other thus allow to achieve
                        synergetic gain.</p>
                </div>
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section {
    background-color: #000000;
    padding: 120px 0;
    color: white;
    font-family: Poppins;
}
.box{
    display: flex;
    align-items: center;
    gap: 100px;
}
.title {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 3px solid #292929;
    padding-bottom: 50px;
    margin-bottom: 50px;
}

.title>h1 {
    font-size: 36px;
    font-weight: 500;
}

.title>p {
    display: none;
}

.text {
    position: relative;
    gap: 90px;
    display: flex;
    align-items: center;
    justify-content: end;
    border-bottom: 3px solid #292929;
    padding-bottom: 50px;
    margin-bottom: 50px;
    overflow: hidden;
}

.text>h1 {
    font-size: 36px;
    font-weight: 500;
}

.text-title>h2 {
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 8px;
    width: 450px;
}

.text-title>p{
    display: none;
}

.last {
    margin-bottom: 0;
    border-bottom: none;
    padding-bottom: 0;
}
@media (max-width:1450px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }

}
@media (max-width:600px){
    .text-title > h2{
        font-size: 14px;
    }
    .text{
        gap: 0px ;
    }
}
@media (max-width:450px){
    .text-title > h2{
        font-size: 12px;
    }
    .text{
        gap: 0px ;
    }
}
@media (max-width:400px){
    .text-title > h2{
        font-size: 10px;
    }
    .text{
        gap: 0px ;
    }
}
</style>

<script setup>
import Container from "../layout/index.vue";
</script>
