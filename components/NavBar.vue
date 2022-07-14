<template>
<div>
  <b-navbar toggleable="lg" type="dark" variant="light" >
    <b-navbar-brand class="text-dark"><Nuxt-link to="./"><img src="../assets/logo.png" class="logo-size" alt="logo"></Nuxt-link>
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav >
      <b-navbar-nav class="ml-auto">
        <b-button class="btn-custom-header py-2"> <NuxtLink to="#" style="color:white;"> Find a Property</NuxtLink></b-button>
        <b-nav-item> <NuxtLink to="#"> Why Alterstay</NuxtLink></b-nav-item>
        <b-nav-item> <NuxtLink to="#"> Be An Alterstay </NuxtLink></b-nav-item>
        
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<style>
.logo-size{
  width: 250px;
  height: 75px;
}

.navbar-toggler-icon{
  filter: invert(1);
}

.navbar-dark .navbar-nav .nav-link{
    color:black!important;
}

.navbar-dark .navbar-nav .nav-link:hover{
    color:rgb(56, 56, 56)!important;
    transition: 0.5; 
}

.btn-custom-header{
    color: white;
    background-color: #3D5C60;
}
a{
  color: black;
}

a:hover{
  color: #3D5C60;
  transition: 0.5;
  text-decoration: none;
}

@media (max-width:768px) {   
.logo-size{
  width: 150px;
  height: 50px;
}

}
</style>

