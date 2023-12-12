<template>

    <div class="all-page">
        <div class="pdf-viewer">
            <object data="./mickael_aitelli_cv.pdf" type="application/pdf" width="100%" height="1200px">
            <embed src="./mickael_aitelli_cv.pdf" type="application/pdf" />
            </object>
        </div>
    </div>

</template>


<script>
    export default {
        name: 'ProjectPage',
        data() {
        }
    };
</script>


<style scoped>

    body {
        font-family: 'preconecct', sans-serif; /* Remplacez 'NouvellePolice' par le nom de la police souhaitée */
        color: #8c3232; /* Remplacez #333 par le code couleur de votre choix */
    }
    .all-page {
        /* margin-left: 15%; */
    }
    .pdf-viewer {
    width: 100%;
    aspect-ratio: 8.5 / 11;
    max-width: 800px;
    margin: auto;
    border: 1px solid #ddd;
}
    embed {
        border: 1px solid #ddd; /* Ajoutez une bordure autour du PDF si nécessaire */
    }
</style>
