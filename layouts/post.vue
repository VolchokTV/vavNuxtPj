<template>
    <div class="wrapper">
      <header>
        <nav>
            <ul>
              <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink to="/posts">Posts</NuxtLink></li>
            </ul>
        </nav>
      </header>
      <AppMenu />
      <div class="container">
        <slot />
      </div>
      <footer>Post Footer В.А.В</footer>
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
    display: flex;
    height: 100px;
    background-color: lightgrey;
    color: greenyellow;
    font-size: 32px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  nav{justify-content: left;}
  </style>