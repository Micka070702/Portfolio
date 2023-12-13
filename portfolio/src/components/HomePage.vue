<template>
    <div class="home">
        <div class="name">
            <h1>Mickael Aïtelli</h1>
        </div>
        <div class="description">
            <p class="subtitle">{{ dynamicText }}</p>
        </div>
    </div>
</template>


<script>
    export default {
        name: 'HomePage',
        data() {
            return {
                descriptionText: "Developer Student at Epitech . . .",
                dynamicText: "",
                loopInterval: null,
                loopDelay: 8000, // Set the delay for the loop in milliseconds
            };
        },
        mounted() {
            this.startTypingAnimation();
        },
        methods: {
            startTypingAnimation() {
                this.typeWriter();
                this.loopInterval = setInterval(() => {
                    this.dynamicText = "";
                    this.typeWriter();
                }, this.loopDelay);
            },
            typeWriter() {
                const speed = 150; // Adjust the typing speed in milliseconds
                let i = 0;
                const text = this.descriptionText;
                const typeInterval = setInterval(() => {
                    this.dynamicText += text.charAt(i);
                    i++;
                    if (i === text.length) {
                        clearInterval(typeInterval);
                    }
                }, speed);
            },
        },
        beforeUnmount() {
            clearInterval(this.loopInterval);
        },
    };
</script>


<style scoped>
    .home {
        text-align: center;
        margin-top: 200px;
    }

    .name h1 {
        font-size: 5em;
        margin-bottom: 10px;
        color: #ffff; /* Adjust color as needed */
    }

    .description {
        margin-top: 10px;
    }

    .subtitle {
        font-size: 2em;
        font-style: italic;
        color: #D1CCDC; /* Adjust color as needed */
        white-space: nowrap; /* Prevent line breaks */
    }
</style>
