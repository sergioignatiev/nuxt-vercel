<template>
  
  <div class="container" v-show="data">
   <NuxtLink to="/fetch">Назад</NuxtLink>
   <h1 class="id title">{{ product.title }}</h1>
    <h4>{{ product.description }}</h4>
    <img :src="product.image" :alt="product.title" class="id-img">
<p class="id-price">Цена:{{ product.price }}$</p>
  </div>
</template>

<script  setup>
const  route = useRoute();
const { data, pending, error, refresh } = await useFetch('https://fakestoreapi.com/products',{})
const product=computed(()=>{
 if(data.value) {return data.value.find(f=>f.id=route.params.id)}
else{
  return {title:"Возникли проблемы с интернетом",
    description:'Попробуйте перезагрузить страницу',
    image:"@/assets/images/error.jpg"
  }
}
}

)

</script>

<style>
.id-img {
 width: 400px;
 max-width:100vw;
}
.id-price {
  font-weight: 900;
}
</style>