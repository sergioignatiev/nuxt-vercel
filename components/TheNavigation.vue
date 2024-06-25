<template>

        <ul class="nav-ul">
            <li class="nav-li"><NuxtLink to="/">Главная</NuxtLink></li>
            <li class="nav-li"><NuxtLink to="/fetch">API</NuxtLink></li>
            <li class="nav-li"><NuxtLink to="/todo">todo</NuxtLink></li>
        </ul>
      
        
  
</template>

<script setup>

</script>

<style  scoped>

.nav-ul {
    padding:10px 0px;
    display:flex;
    list-style-type: none;
    border-bottom: 1px solid lightgrey; 
}
.nav-li a {
 display:block;
 text-decoration: none;
 margin:0px 20px;
color:black;
 text-transform: uppercase
}
a.router-link-active {
   opacity: 0.5;
  }
</style>