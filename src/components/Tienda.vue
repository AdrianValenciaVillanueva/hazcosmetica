<template>
    <b class="Shop-title">Tienda</b>
    
</template>
<script>
export default {
    name: "TiendaMenu"
}</script>
<style>

.Shop-title{
    font-size: 2.4rem;
    font-weight: 700; 
    position: relative;
    display: inline-block;
    margin-bottom: 1rem;
}

.Shop-title::after {
    content: '';
    width: 130px;
    height: 50px;
    background-image: url('@/assets/Vector.png'); 
    background-size: contain; 
    background-repeat: no-repeat; 
    display: block;
    margin: -1rem -.5rem 0 auto;
  }
</style>