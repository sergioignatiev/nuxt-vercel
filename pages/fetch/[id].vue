<template>
  
  <div class="container id" v-show="data">
   <NuxtLink to="/fetch">&larr; Назад</NuxtLink>
   <h1 class="id title">{{ product.title }}</h1>
    <h4>{{ product.description }}</h4>
    <img :src="product.image" :alt="product.title" class="id-img">
<p class="id-price">Цена:{{ product.price }}$</p>
  </div>
</template>

<script  setup>
const  route = useRoute();
const id=route.params.id
const url='https://fakestoreapi.com/products/'
const { data } = await useFetch(url)
const product=computed(()=>{
return data.value[id-1]


}

)

</script>

<style>
.id{
  padding:20px;
}
.id-img {
 width: 400px;
 max-width:100vw;
}
.id-price {
  font-weight: 900;
}
</style>