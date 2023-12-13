<template>

    <div class="wrap">
        <div class="pdf-viewer">
            <object data="./mickael_aitelli_cv.pdf" type="application/pdf" width="100%" height="1200px">
                <embed src="./mickael_aitelli_cv.pdf" type="application/pdf" />
            </object>
        </div>
        <a :href="pdfPath" download="mickael_aitelli_cv.pdf">
            <button class="download">Download</button>
        </a>
    </div><br><br><br>
</template>


<script>
    export default {
        name: 'ProjectPage',
        data() {
            return {
                pdfPath: './mickael_aitelli_cv.pdf',
            };
        },
    };
</script>


<style scoped>
    .pdf-viewer {
        width: 100%;
        aspect-ratio: 8.5 / 11;
        max-width: 800px;
        margin: auto;
        margin-top: 50px;
        border: 1px solid #ddd;
    }
    button.download {
        margin-top: 10px;
        padding: 10px;
        background-color: #8A4FFF;
        border-radius: 5px;
        border: 1px solid #000000;
        color: white;
    }
    button.download:hover {
        background-color: #7241d3;
        /* border: 1px solid #c8c8c8; */
        color: white;
    }

</style>
