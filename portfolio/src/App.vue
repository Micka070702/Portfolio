<template>

    <Header></Header>
    <router-view/>
    <Footer></Footer>

</template>


<script>

    import Header from './components/Header'
    import Footer from './components/Footer'

    export default {
        components: {
            Header,
            Footer
        }
    }

</script>


<style>

    body {
        margin: 0 auto;
        background-color: #1E1042;
    }
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;

        text-align: center;
        color: #D1CCDC;
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }
    .footer {
        margin-top: auto;
    }

</style>
