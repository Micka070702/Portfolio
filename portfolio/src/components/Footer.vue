<template>

    <footer class="footer">

        <div class="footer-content">
            <b>&copy; 2023</b>
            <p class="link-group">Mickael Aïtelli</p>
        </div>

        <div class="footer-content">
            <b>Me Contacter</b>
            <div class="link-group">
                <a href="https://www.linkedin.com/in/micka%C3%ABl-a%C3%AFtelli-39000a246/">Linkedin</a>
            </div>
        </div>

        <div class="footer-content">
            <b>Mes réseaux</b>
            <div class="link-group">
                <a href="https://www.linkedin.com/in/micka%C3%ABl-a%C3%AFtelli-39000a246/">Linkedin</a>
                <a href="https://www.instagram.com/micka.aitelli/?hl=fr">Instagram</a>
            </div>
        </div>

        <div class="footer-content">
            <b>Navigation</b>
                <ul class="link-group">
                    <router-link to="/">Home</router-link>
                    <router-link to="/about">About</router-link>
                    <router-link to="/project">Project</router-link>
                    <!-- Ajoutez d'autres liens de navigation si nécessaire -->
                </ul>
        </div>

    </footer>

</template>


<script>

    export default {
        name: 'MyFooter',
    };

</script>


<style scoped>
    .footer {
        display: flex;
        color: white;
        background-color: #1a303f;
        border-top: 2px solid #81cfe0;
        padding-top: 20px;
        padding-bottom: 20px;
        width: 100%;
        margin-top: 100px;
    }
    .footer-content {
        display: inline-block;
        margin-right: 50px;
        text-align: left;
    }
    .footer-content:first-child {
        margin-left: 10%;
    }
    .link-group a {
        display: block;
        color: #81cfe0;
        text-decoration: none;
    }

    .link-group {
        font-weight: bold;
        list-style-type: none;
        padding: 0;
        margin: 10px 0 0;
    }


</style>
