<template>

        <ul class="nav-ul">
            <li class="nav-li"><NuxtLink to="/">Главная</NuxtLink></li>
            <li class="nav-li"><NuxtLink to="/fetch">API</NuxtLink></li>
        </ul>
      
        
  
</template>

<script setup>

</script>

<style  scoped>
.nav {

}
.nav-ul {
    display:flex;
    list-style-type: none;
    
}
.nav-li a {
 display:block;
 text-decoration: none;
 margin:0px 20px;
 color:red;
 text-transform: uppercase
}
</style>