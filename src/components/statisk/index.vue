<template>
  <section>
        <Container>
          <div class="title">
            <h1>Ko'rsatkichlar</h1>
            <div class="cards">
              <div class="card-1">
                <h2>253 030</h2>
                <p>Tashabbuslar soni</p>
              </div>
              <div class="card-1">
                <h2>70 789</h2>
                <p>Sertifikat olganlar soni</p>
              </div>
              <div class="card-1">
                <h2>49 462</h2>
                <p>Kredit olganlar soni</p>
              </div>

            </div>
          </div>

          <div class="wrapper">
            <table>
              <thead>
                <tr class="head">
                  <th class="wide left">Viloyat nomi</th>
                  <th class="wide right">Banklar kesimida</th>
                </tr>
                <tr class="line">
                  <th class="main">Viloyat nomi</th>
                  <th class="medium">Ariza soni</th>
                  <th class="medium">Jami summa</th>
                </tr>
              </thead>
              <tbody>
                <tr class="line">
                  <td class="main">1</td>
                  <td class="medium">1</td>
                  <td class="medium">1</td>
                </tr>
                <tr class="line">
                  <td class="main">2</td>
                  <td class="medium">2</td>
                  <td class="medium">2</td>
                </tr>
                <tr class="line">
                  <td class="main">3</td>
                  <td class="medium">3</td>
                  <td class="medium">3</td>
                </tr>
                <tr class="line">
                  <td class="main">4</td>
                  <td class="medium">4</td>
                  <td class="medium">4</td>
                </tr>
                <tr class="line">
                  <td class="main">5</td>
                  <td class="medium">5</td>
                  <td class="medium">5</td>
                </tr>
                <tr class="line">
                  <td class="main bottom-right">6</td>
                  <td class="medium">6</td>
                  <td class="medium bottom-left">6</td>
                </tr>
              </tbody>
            </table>
          </div>
        </Container>
      </section>
</template>

<style scoped>
section {
  background-color: #F9F9FB;
  padding: 40px 0 80px;
  font-family: Poppins, sans-serif;
}

.title>h1 {
  margin-bottom: 40px;
  font-size: 36px;
  font-weight: 500;
  color: #26252B;
}

.cards {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.card-1 {
  padding: 24px;
  width: 432px;
  height: 129px;
  background-color: white;
  border-radius: 24px;
}

.card-1>h2 {
  color: #72C420;
  font-size: 36px;
  font-weight: 500;
  margin-bottom: 10px;
}

.card-1>p {
  opacity: 0.7;
}

table {
  margin-top: 50px;
  width: 100%;
  border-collapse: collapse;
}

.left {
  border-top-left-radius: 20px;
}

.right {
  border-top-right-radius: 20px;
  background-color: white;
  color: black;
}

.line>th {
  display: block;
  background-color: white;
  color: black;
  display: flex;
}

.line {
  background-color: white;
  display: flex;
}

.bottom-right {
  border-bottom-left-radius: 20px;
}

.bottom-left {
  border-bottom-right-radius: 20px;
}

.medium {
  width: 340px;
  border-top-right-radius: 0;
  display: flex;
}

.main {
  width: 680px;
  display: flex;
}

thead th {
  background-color: #7CD33D;
  color: white;
  padding: 15px;
  text-align: center;
  font-weight: 600;
  border: 1px solid #e0e5f2;
}

.head {
  display: flex;
}

thead th.wide {
  display: block;
  width: 50%;
}

tbody td {
  padding: 15px;
  border: 1px solid #e0e5f2;
  text-align: center;
}
@media (max-width:1420px){
  .container{
      width: 100%;
      max-width: 992px;
      padding: 0 15px;
  }
  .card-1{
    width: 315px;
    height: 129px;
  }

  .main{
    width: 280px;
  }
}
@media (max-width:992px){
  .title{
    padding: 0 40px;
  }
  .cards{
    gap: 8px;
  }
  .wrapper{
    padding: 0 40px;
  }
  .main{
    width: 50%;
  }
}
@media (max-width:768px){
  .cards{
    flex-direction: column;
  }
  .card-1{
    width: 100%;
    overflow: hidden;
  }
  .head{
    width: 100%;
  }
  .medium{
    width: 45%;
  }
  .main{
    width: 95%;
  }
}
@media (max-width:400px){
  th{
    font-size: 12px;
  }
}
</style>

<script setup>
import Container from "../layout/index.vue"
</script>