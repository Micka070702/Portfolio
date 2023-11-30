<template>
    <div class="project">
      <img
        alt="Vue logo"
        src="../assets/kc.jpeg"
        style="width: 100%; height: auto;"
      />
      <HelloWorld msg="Welcome to Your Vue.js App" />
    </div>
  </template>

<script>
    // @ is an alias to /src
    import HelloWorld from '@/components/ProjectPage.vue'

    export default {
        name: 'ProjectView',
        components: {
            HelloWorld
        }
    }
</script>