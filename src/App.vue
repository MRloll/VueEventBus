<template lang="pug">
#app
    tabs-bar
    parent-wrapper
</template>

<script>
import TabsBar from "./components/TabsBar.vue";
import ParentWrapper from "./components/ParentWrapper.vue";

export default {
    name: "App",
    components: {
        TabsBar,
        ParentWrapper,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
