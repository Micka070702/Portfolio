<!-- Header.vue -->
<template>
    <header class="header">
        <nav>
            <ul>
                <li class="micka"><router-link to="/">MICKAEL AITELLI</router-link></li>
                <li><router-link to="/project">Project</router-link></li>
                <li><router-link to="/cv">Cv</router-link></li>
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
    .header {
        background-color:#170C31;
        text-align: left;
        padding: 30px;
    }
    .micka {
        margin-left: 10%;
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
