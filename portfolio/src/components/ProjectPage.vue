<template>

    <div class="all-page">
        <div class="main-title">
            <br><br><br><br><br>
            <h1> Personal Projects</h1>
            <p>Ci-dessous, mes projets personels ou, aux quels j'ai pu participer.</p><br>
        </div>

        <div class="all_project">
            <div v-for="personal_project in personal_projects" :key="personal_project.id" class="project">
                <div class="project-cases">
                    <div class="img-container">
                        <img class="img" :alt="personal_project.title" :src="require('@/assets/' + personal_project.image)">
                    </div>
                    <div class="project-text">
                        <h3>{{ personal_project.title }}</h3>
                        <p v-html="personal_project.description"></p>

                        <div class="project-tech">
                            <span v-for="(tech, index) in personal_project.tech" :key="index" class="tech-indiv">{{ tech }}{{ index < personal_project.tech.length - 1 ? '   ' : '' }}</span>
                        </div>
                        <div class="buttons">
                            <a class="github-link-container" :href="personal_project.githublink">
                                <img class="github-link" :src="require('@/assets/githublogo.png')" alt="GitHub Logo" />
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="main-title2">
            <br><br><br><br><br>
            <div class="title-container">
                <h1 class="ep_pj">Epitech projects</h1>
                <img class="epitech_img" :alt="Epitech" :src="require('@/assets/epitech.png')">
            </div>
            <p>Ci-dessous, des projets que j'ai pu faire ou aux quels j'ai participé au seins d'Epitech.</p><br>
        </div>

        <div class="all_project">
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
                personal_projects: [
                    {
                        id: 1,
                        title: 'nothing',
                        description: 'Time: ...<br>....<br><br>Fonctionnalités clés incluant: ...',
                        tech: ['Nothing'],
                        image: 'comingsoon.jpeg',
                        githublink: "."
                    }
                ],

                projects: [
                    {
                        id: 1,
                        title: 'My paint',
                        description: 'Time: 3 weeks<br>Recréation de Paint en équipe de deux.<br><br>Fonctionnalités clés incluant: tracé de lignes, remplissage, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyPaint.png',
                        githublink: "https://github.com/EpitechPromo2027/B-MUL-200-MAR-2-1-mypaint-nino.litim"
                    },
                    {
                        id: 2,
                        title: 'My RPG',
                        description: 'Time: 4 weeks<br>Création d\'un RPG en équipe de 4.<br><br>Fonctionnalités clés incluant: Caractéristiques, Combats, et sélection de couleurs.',
                        tech: ['C', 'CSFML'],
                        image: 'miniaMyRPG.png',
                        githublink: "https://github.com/EpitechPromo2027/B-MUL-200-MAR-2-1-myrpg-nino.litim"
                    }
                ]
            };
        }
    };
</script>


<style scoped>

    body {
        font-family: 'preconecct', sans-serif; /* Remplacez 'NouvellePolice' par le nom de la police souhaitée */
        color: #8c3232; /* Remplacez #333 par le code couleur de votre choix */
    }
    .all-page {
        margin-left: 15%;
    }
    .main-title {
        text-align: left;
    }
    .main-title2 {
        display: flex;
        flex-direction: column;
        align-items:start;
    }
    .title-container {
        display: flex;
        justify-content: start;
    }
    .ep_pj {
        order: 2;
    }
    .epitech_img {
        order: 1;
        width: 30px;
        height: 30px;
        margin-top: 27px;
        margin-right: 10px;
    }
    .all_project {
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
        border: 2px solid #8A4FFF;
        border-radius: 11px;
        height: 100%;
        background-color: #170C31;
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
        background-color: #390040;
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
    background-color: #390040;
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
