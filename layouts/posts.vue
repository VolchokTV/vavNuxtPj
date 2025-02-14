<template>
    <div class="wrapper">
      <header>
        <nav>
            <ul>
              <li><NuxtLink to="/">Home</NuxtLink></li>
              <li><NuxtLink to="/about">About</NuxtLink></li>
            </ul>
        </nav>
      </header>
      <AppMenu />
      <div class="container">
        <slot />
      </div>
      <footer>Posts Footer В.А.В</footer>
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
  header,
  footer {
    height: 100px;
    background-color: lightgrey;
    color: red;
    font-size: 32px;
    display: flex;
    justify-content: left;
    align-items: center;
  }

  nav ul li{
    display: inline-block;
    list-style: none;    
    padding-right: 20px    
  }

  </style>