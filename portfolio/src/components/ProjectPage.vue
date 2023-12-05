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
                        <p v-html="project.description"></p>

                        <div class="project-tech">
                            <span v-for="(tech, index) in project.tech" :key="index" class="tech-indiv">{{ tech }}{{ index < project.tech.length - 1 ? '   ' : '' }}</span>
                        </div>
                        <div class="buttons">
                            <a class="github-link-container" :href="project.githublink">
                                <img class="github-link" :src="require('@/assets/githublogo.png')" alt="GitHub Logo" />
                            </a>
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
                        description: 'Recréation de Paint en équipe de deux.<br>Time: 3 weeks<br><br>Fonctionnalités clés incluant: tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyPaint.png',
                        githublink: "https://github.com/EpitechPromo2027/B-MUL-200-MAR-2-1-mypaint-nino.litim"
                    },
                    {
                        id: 2,
                        title: 'My RPG',
                        description: 'Création d\'un RPG en équipe de 4.<br>Travail effectué en environ quatres semaines.<br><br>Fonctionnalités clés incluant: Caractéristiques, Combats, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyRPG.png',
                        githublink: "https://github.com/EpitechPromo2027/B-MUL-200-MAR-2-1-myrpg-nino.litim"
                    },
                    {
                        id: 3,
                        title: 'My RPG',
                        description: 'Création d\'un RPG en équipe de 4.<br>Travail effectué en environ quatres semaines.<br><br>Fonctionnalités clés incluant: Caractéristiques, Combats, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyRPG.png',
                    }
                ]
            };
        }
    };
</script>


<style scoped>

    body {
        font-family: 'NouvellePolice', sans-serif; /* Remplacez 'NouvellePolice' par le nom de la police souhaitée */
        color: #333; /* Remplacez #333 par le code couleur de votre choix */
    }
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
        height: auto;
    }
    .project-cases {
        display: flex;
        flex-direction: column;
        border: 1px solid rgba(230, 0, 255, 0.6);
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
        margin-left: 35px;
        height: 40%;
    }
    .project-tech span {
        margin-right: 15px;
    }
    .tech-indiv {
        border-radius: 4px;
        background-color: rgba(230, 0, 255, 0.5);
        padding-left: 3px;
        padding-right: 3px;
    }
    .buttons {
        display: flex;
        justify-content: right;
        align-items: center;
        margin-top: 10%;
        margin-bottom: 20px;
        margin-right: 30px;
    }
    .github-link-container:hover .github-link {
    background-color: rgba(185, 115, 236, 0.432);
    border-radius: 3px;
    padding: 4px;
    /* transform: scale(1.1); */
    transition: 0.3s;
    margin: -4px;
}
    .github-link {
        width: 25px;
        /* Supprimez le positionnement relatif et les décalages */
    }
</style>
