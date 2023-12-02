<!-- Header.vue -->
<template>
    <header class="header">
      <nav>
        <ul>
          <li><router-link to="/">MICKAEL AITELLI</router-link></li>
          <li><router-link to="/about">À propos</router-link></li>
          <li><router-link to="/project">Project</router-link></li>
          <!-- Ajoutez d'autres liens de navigation si nécessaire -->
        </ul>
      </nav>
    </header>
  </template>

  <script>
  export default {
    name: 'My-Header',
  };
  </script>

  <style scoped>
  /* Ajoutez du style pour votre en-tête ici */
  .header {
    background-color:#111827;
    text-align: right;
    margin-right: 3%;
    padding: 30px;
  }

  nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
  }

  nav li {
    display: inline-block;
    margin-right: 20px;
  }

  nav a {
    text-decoration: none;
    color: rgb(255, 255, 255);
    font-weight: bold;
  }
  </style>
