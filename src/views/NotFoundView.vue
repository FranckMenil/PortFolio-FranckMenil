<template>
    <div class="not-found">
      <img src="/src/assets/pictures/ORFI0N0.jpg" alt="404">
      <h1>404 - Page Not Found</h1>
      <router-link to="/">Retour à l'accueil</router-link>
    </div>
  </template>
  
  <style scoped>
  .not-found {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    text-align: center;
  }
  
  .not-found img {
    max-width: 100%;
    height: auto;
  }
  
  .not-found h1 {
    font-size: 3rem;
    margin: 1rem 0;
  }
  </style>
  