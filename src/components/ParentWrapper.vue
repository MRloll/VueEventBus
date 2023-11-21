<template lang="pug">
.parent-wrapper  #[h2 parent component]
    child-component
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
    components: {
        ChildComponent,
    },
};
</script>

<style lang="scss" scoped>
.parent-wrapper {
    border: 1px solid #333;
    border-radius: 10px;
    max-width: 600px;
    margin: auto;
    padding: 100px;
    background: #fce4e4;
}
</style>