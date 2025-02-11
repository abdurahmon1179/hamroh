<template>
    <section>
        <Container>
            <div class="wrapper" id="forwho">
                <div class="banner">
                    <div class="card-1 card">
                        <p>O‘z biznes rejasiga ega tadbirkorlar</p>
                        <b>518</b>
                    </div>
                    <div class="card-2 card">
                        <p>Sertifikat olganlar</p>
                        <b>208</b>
                    </div>
                    <div class="card-3 card">
                        <p>Imtiyozli kredit olganlar</p>
                        <b>102</b>
                    </div>
                    <div class="card-4 card">
                        <p>Kichik biznes subyektlari</p>
                        <b>230</b>
                    </div>
                    <div class="card-5 card">
                        <p>Ro'yhatdan o'tganlar</p>
                        <b>5 208</b>
                    </div>
                </div>
                <div class="text">
                    <h1>Dasturda kimlar ishtirok etishi mumkin?</h1>
                    <p>Kamida bir yil davomida faoliyat yuritib, ikki yoki undan ortiq kishini doimiy ish bilan
                        ta‘minlayotgan ijobiy kredit tarixiga ega kichik va o'rta tadbirkorlik subyektlari</p>
                </div>
            </div>
        </Container>

        <!-- id lar sectionga beriladi -->
        <!-- intro rasmlar tugirlash -->
        <!-- table rowlar tugirlash -->
        <!-- burger menu tugirlash -->
        <!-- intro height -->
    </section>
</template>

<style scoped>
section {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #F2F8D8;
    height: 800px;
    margin-top: -20px;
    padding: 120px 0;
    font-family: Poppins;
    overflow: hidden;
}
.wrapper {
    font-family: Arial, Helvetica, sans-serif;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.text>h1 {
    font-size: 36px;
    font-weight: 500;
    margin-bottom: 12px;
    width: 600px;
}
.text>p {
    width: 590px;
    line-height: 22px;
    margin-bottom: 32px;
}
.banner{
    background-image: url(../../../public/img/woman-circle.png);
    background-repeat: no-repeat;
    width: 620px;
    height: 560px;
    position: relative;
}
.card-1{
    position: absolute;
    top: 0;
    right: 100px;
}
.card-2{
    position: absolute;
    top: 150px;
}
.card-3{
    position: absolute;
    bottom: 150px;
    left: 0;
}
.card-4{
    position: absolute;
    right: 0px;
    top: 250px;
}
.card-5{
    position: absolute;
    right: 100px;
    bottom: 50px;
}
.card{
    background-color: white;
    border: 1px solid #eeedf3;
    border-radius: 16px;
    padding: 12px 20px;
}
@media (max-width:1420px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }
    img{
        width: 560px;
        height: 560px;
    }
    .text > h1{
        font-size: 36px;
        font-weight: 500;
        width: 300px;
    }
    .text > p{
        line-height: 140%;
        width: 330px;
    }
}
@media (max-width:992px){
    .banner > img{
        width: 400px;
        height: 400px;
    }
    .wrapper{
        padding: 0 40px;
    }
    .text > h1{
        width: 400px;
        font-size: 36px;
    }
    .text > p{
        width: 400px;
        line-height: 140%;
    }
}
@media (max-width:768px){
    .wrapper{
        flex-direction: column;
    }
    .text > h1{
        width: 100%;
        font-size: 24px;
        text-align: center;
    }
    .text > p{
        font-size: 16px;
        width: 102%;
        text-align: center;
    }
}
</style>

<script setup>
import Container from "../layout/index.vue"
</script>