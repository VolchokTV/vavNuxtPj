<template>
    <div class="wrapper">
      <header>
        <h2>В.А.В NUXT 3 Home Work</h2>        
      </header>
      <AppMenu />
      <div class="container">
        <slot />
      </div>
      <footer>В.А.В 2025 NUXT 3 Home Work (c)</footer>
    </div>
  </template>
  
  <script setup lang="ts"></script>
  
  <style scoped>
  .wrapper {
    display: flex;
    flex-direction: column;
    min-height: 100dvh;
    justify-content: space-between;
  }
  .container {
    flex-grow: 1;
  }
  header
  {
    height: 100px;
    background-color: lightgrey;
    color: black;
    font-size: 28px;
    display: flex;
    justify-content: center;
    align-items: center;
    
  }

  footer {
    height: 100px;
    background-color: lightgrey;
    color: black;
    font-size: 28px;
    display: flex;
    justify-content: center;
    align-items: center;
    
  }

  nav ul li{
    display: inline-block;
    list-style: none;    
    padding-right: 20px;
    color: brown;
  }

  nav {
    display: inline-block;
    padding-left: 20px;
    justify-content: left;
    
  }

  </style>