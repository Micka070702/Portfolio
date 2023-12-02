<template>

    <div class="all-page">
        <div class="main-title">
            <h1>Projets</h1>
            <p>Ci-dessous, des projets que j'ai pu faire ou aux quels j'ai participé.</p>
        </div>

        <div class="all-project">
            <div v-for="project in projects" :key="project.id" class="project">
                <div class="project-cases">
                    <div class="img-container">
                        <img class="img" :alt="project.title" :src="require('@/assets/' + project.image)">
                    </div>
                    <div class="project-text">
                        <h3>{{ project.title }}</h3>
                        <p>{{ project.description }}</p>

                        <div class="project-tech">
                            <p>{{ project.tech }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>


<script>
    export default {
        name: 'ProjectPage',
        data() {
            return {
                projects: [
                    {
                        id: 1,
                        title: 'My paint',
                        description: 'Recréation de Paint en équipe de deux.Travail effectué en environ trois semaines. Fonctionnalités clés incluant tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: 'Vue.js',
                        image: 'miniaMyPaint.png'
                    },
                    {
                        id: 2,
                        title: 'Project test 1',
                        description: 'Recréation de Paint en équipe de deux.Travail effectué en environ trois semaines. Fonctionnalités clés incluant tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: 'Vue.js',
                        image: 'miniaMyPaint.png'
                    },
                    {
                        id: 3,
                        title: 'Project test 1',
                        description: 'Recréation de Paint en équipe de deux.Travail effectué en environ trois semaines. Fonctionnalités clés incluant tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: 'Vue.js',
                        image: 'miniaMyPaint.png'
                    }
                ]
            };
        }
    };
</script>


<style scoped>
    .all-page {
        margin-left: 10%;
    }
    .main-title {
        text-align: left;
    }
    .all-project {
        display: flex;
        flex-wrap: wrap;
    }
    .project {
        width: 44%;
        margin-bottom: 0.8%;
        margin-right: 0.8%;
        height: 600px; /* Hauteur fixe des projet */
    }
    .project-cases {
        display: flex;
        flex-direction: column;
        border: 1px solid #20283b;
        border-radius: 9px;
        height: 100%; /* Remplir la hauteur du projet */
        background-color: #000a28;
    }
    .img-container {
        overflow: hidden;
        height: 60%; /* Ajuster la hauteur de l'image */
    }
    .img {
        width: 100%;
        height: 100%;
        border-top-left-radius: 9px;
        border-top-right-radius: 9px;
    }
    .project-text {
        text-align: left;
        margin-left: 2%;
        height: 40%; /* Ajuster la hauteur du texte */
    }
  </style>
