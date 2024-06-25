<template>
  <div class="container card">
    <h1 class="card-title-mobile mobile">Бунинь</h1>
    <h2 class="card-second-title-mobile mobile">Иван Алексеевич</h2>
    <img src="https://upload.wikimedia.org/wikipedia/commons/1/1a/Ivan_Bunin_%28sepia%29.jpg" alt="bunin" class="card-image">
 <div class="card-info">
    <h1 class="card-title">Бунин</h1>
 <h2 class="card-second-title">Иван Алексеевич</h2>
<p class="card-p"> Бунин рано начал самостоятельную жизнь; в юношеские годы работал в газетах, канцеляриях, много странствовал. 
</p>
    <p class="card-p">Первый стихотворный сборник вышел в свет в 1891 году в Орле.</p>
<p class="card-p">В 1933 году Бунин — первым из русских писателей — стал лауреатом Нобелевской премии по литературе за «строгое мастерство, с которым он развивает традиции русской классической прозы».
</p>
    <p class="card-p">Скончался в 1953 году, похоронен на кладбище Сент-Женевьев-де-Буа.</p>
<div class="card-contacts">
    <div class="card-contacts-phone">тел.: +7 (757) 987-76-78</div>
    <div class="card-contacts-gma">email.: IvanBynin@gmail.com</div>
</div> 
</div>
 </div>
 
</template>

<script setup>

</script>

<style  scoped>
*{
    margin: 0;
padding: 0;
box-sizing: border-box;
}
.container {
}
.mobile{
    display:none;
}
.card {
    display:flex;
    margin:30px;
    font-family:Arial, Helvetica, sans-serif;
}
.card-image {
    width:40vw;
}
.card-info {

    padding-left: 20px;
    display:flex;
    flex-direction: column;
    justify-content: space-between
}
.card-title {
    font-size: 150px;
   
}
.card-second-title {
    font-size: 70px;
}
.card-p {
    font-size:20px;
}
.card-contacts {
    font-weight: bold;
}
.card-contacts-phone {
}
.card-contacts-gma {
}
@media (max-width:800px) {
   .mobile{
    display:block;
    
   }
   .card-title-mobile{
    font-size: 70px;
   }
   .card-second-title-mobile{
    font-size: 50px;
   }
    .card{
        flex-direction: column;
        margin:10px;
    }
    .card-image{
        width:100%;
    }
    .card-info{
        padding-left: 0;
    }
    .card-title ,.card-second-title {
        display:none;
    }
    .card-p{
        padding-top: 20px;
    }
    .card-contacts{
        margin-top: 20px;
    }
}
</style>