<template>
    <section>
        <Container>
            <h1>Yangiliklar</h1>
            <div class="wrapper">
                <div class="card">
                    <img src="../../../public/img/cardimage.png" alt="">
                    <p>20 марта 2024</p>
                    <h2>HAMROH.uz</h2>
                    <div class="btn">
                        <button>Batafsil</button>
                    </div>
                </div>

                <div class="card">
                    <img src="../../../public/img/cardimage.png" alt="">
                    <p>2025-01-09</p>
                    <h2>HAMROH.uz</h2>
                    <div class="btn">
                        <button>Batafsil</button>
                    </div>
                </div>

                <div class="card">
                    <img src="../../../public/img/cardimage.png" alt="">
                    <p>20 марта 2024</p>
                    <h2>HAMROH.uz</h2>
                    <div class="btn">
                        <button>Batafsil</button>
                    </div>
                </div>

                <div class="card none">
                    <img src="../../../public/img/cardimage.png" alt="">
                    <p>20 марта 2024</p>
                    <h2>HAMROH.uz</h2>
                    <div class="btn">
                        <button>Batafsil</button>
                    </div>
                </div>
            </div>
        </Container>
    </section>
</template>

<style scoped>
section {
    background-color:  #f9f9fb;
    font-family: Poppins;
    padding: 120px 0;
    /* margin-bottom: 120px; */
}

h1 {
    font-size: 36px;
    font-weight: 500;
    text-align: center;
    margin-bottom: 40px;
}
.none{
    display: none;
}
.card>p {
    margin-top: 20px;
    margin-bottom: 8px;
    color: #3D3D3D;
}

.card>h2 {
    font-size: 20px;
    font-weight: 700;
    width: 400px;
    line-height: 30px;
}
.card{
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    padding: 10px;
    border-radius: 16px;
    background-color: white;
}
.wrapper {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 500px;
    width: 100%;
}
.btn > button{
    width: 142px;
    height: 40px;
    background-color: transparent;
    color: #72c420;
    border: 1px solid #72c420;
    border-radius: 48px;
    cursor: pointer;
}
.btn{
    width: 100%;
    display: flex;
    justify-content: end;
}

@media (max-width:1420px){
    .container{
            width: 100%;
            max-width: 992px;
            padding: 0 15px;
    }
    .card{
        width: 300px;
        padding: 10px;
    }
    .card > img{
        object-fit: contain;
        width: 280px;
    }
}

@media (max-width:992px){
    .card{
        width: 30%;
    }
    .card > img{
        width: 100%;
    }
    .wrapper{
        padding: 0 40px;
    }
    .card > h2{
        font-size: 18px;
    }
    .btn > button{
        width: 55%;
    }
}
@media (max-width:700px){
    .wrapper{
        flex-direction: column;
        gap: 50px;
        height: 100%;
        padding: 0;
    }
    .card{
        width: 90%;
        overflow: hidden;
        max-height: 100%;
        
    }
    .card > img{
        width: 100%;
    }
}
</style>

<script setup>
import Container from "../layout/index.vue"
</script>