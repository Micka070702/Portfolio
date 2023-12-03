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
                        <p v-html="project.description"></p><br>

                        <div class="project-tech">
                            <span v-for="(tech, index) in project.tech" :key="index">{{ tech }}{{ index < project.tech.length - 1 ? '   ' : '' }}</span>
                        </div>
                        <img class="project-type" :src="require('@/assets/' + project.type)">
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
                        description: 'Recréation de Paint en équipe de deux.<br>Travail effectué en environ trois semaines.<br><br>Fonctionnalités clés incluant: tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyPaint.png',
                        type: 'epitech.png'
                    },
                    {
                        id: 2,
                        title: 'My RPG',
                        description: 'Création d\'un RPG en équipe de 4.<br>Travail effectué en environ quatres semaines.<br><br>Fonctionnalités clés incluant: Caractéristiques, Combats, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyRPG.png',
                        type: 'epitech.png'
                    },
                    {
                        id: 3,
                        title: 'My RPG',
                        description: 'Création d\'un RPG en équipe de 4.<br>Travail effectué en environ quatres semaines.<br><br>Fonctionnalités clés incluant: Caractéristiques, Combats, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyRPG.png',
                        type: 'epitech.png'
                    }
                ]
            };
        }
    };
</script>


<style scoped>
    .all-page {
        margin-left: 15%;
    }
    .main-title {
        text-align: left;
    }
    .all-project {
        display: flex;
        flex-wrap: wrap;
    }
    .project {
        width: 40%;
        margin-bottom: 0.8%;
        margin-right: 0.8%;
        height: 600px; /* Hauteur fixe des projet */
    }
    .project-cases {
        display: flex;
        flex-direction: column;
        border: 1px solid #20283b;
        border-radius: 9px;
        height: 100%;
        background-color: #000a28;
    }
    .img-container {
        overflow: hidden;
        width: 100%;
        height: auto;
    }
    .img {
        width: 100%;
        height: auto;
        border-top-left-radius: 9px;
        border-top-right-radius: 9px;
    }
    .project-text {
        text-align: left;
        margin-left: 2%;
        height: 40%;
    }
    .project-tech span {
        margin-right: 15px;
    }
    .project-type {
        width: 30px;
        display: flex;
        position:relative;
        bottom: 5%;
        right: -90%;
    }
  </style>
