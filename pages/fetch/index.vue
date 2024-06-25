<template>
    <h1 v-show="!data">... Ждите,или попробуйте перезагрузить страницу.</h1>
  <div class="container fetch" v-show="data">
<div class="fetch-block" v-for="f in data" :key="f.id">
    
<img :src="f.image" :alt="f.title" class="fetch-image">
<div class="fetch-tit">{{ f.title }}</div>
<NuxtLink :to="`/fetch/${f.id}`" >
    <button class="btn-link">Посмотреть Подробнее</button>
</NuxtLink>

</div> 
  </div>
</template>

<script  setup>
const { data, pending, error, refresh } = await useFetch('https://fakestoreapi.com/products',{
    
})
</script>

<style>

.fetch {
    display: flex;
    flex-wrap: wrap;

}
.fetch-image{
    width:200px;
}
.fetch-block {
  width: 300px;
    margin:20px;
    border-radius: 10px;
   border:1px solid burlywood;
    padding:20px;
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}
.fetch-tit {
    font-family: sans-serif;
    font-weight: 800;
}

.btn-link {
    margin-top:50px;
    padding:10px 20px;
    border:none;
    border-radius: 5px;
    background-color: rgb(5, 145, 96);
    color:white;
    text-transform: uppercase;
}
:hover.btn-link{
    background-color: rgb(2, 135, 106);
}

</style>