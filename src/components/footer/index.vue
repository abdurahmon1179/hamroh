<template>
    <section>
        <Container>
            <div class="wrapper">
                <div class="title">
                <a href=""><img src="../../../public/img/logo.svg" alt=""></a>
            </div>
            <div class="menu">
                <p><b> Murojaat uchun telefon raqam: </b> +998909290801</p>
                <p><b> Manzil: </b> O‘zbekiston, Toshkent shahri, Islom Karimov ko'chasi, 2a</p>
                <p> <b>Elektron manzilimiz:</b>  hamroh@exat.uz</p>
            </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section{
    background-color: #F2F8D8;
    padding: 48px 0;
}
.title{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 40px;
    border-bottom: 3px solid #E0E5F2;
}
.title > a{
    color: black;
    text-decoration: none;
    font-size: 24px;
}
.title > a:hover{
    opacity: 0.5;
}
.menu{
    display: flex;
    align-items: end;
    margin-top: 40px;
    gap: 40px;
}
@media (max-width:1420px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }
}

@media (max-width:992px){
    .wrapper{
        padding: 0 40px;
    }
    .menu > p{
        max-width: 90%;
    }
}
@media (max-width:576px){
    .menu{
        flex-direction: column;
        width: 100%;
    }
    .menu > p{
        text-align: center;
        width: 100%;
    }
}
</style>


<script setup >
import Container from "../layout/index.vue"
</script>