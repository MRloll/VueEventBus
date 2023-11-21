<template lang="pug">
.child-component  #[h2 child component]
    //- given data from tabs-bar
    p data given from tabs bar {{ dataFromTabs }}
</template>


<script>
import { EventBus } from "../main";

export default {
    data() {
        return {
            dataFromTabs: "initial data",
        };
    },
    mounted() {
        // adding eventBus listener
        EventBus.$on("sendPayloadWithEventBus", (payload) => {
            this.dataFromTabs = payload;
        });
    },
    beforeDestroy() {
        // removing eventBus listener
        EventBus.$off("sendPayloadWithEventBus");
    },
};
</script>

<style lang="scss" scoped>
.child-component {
    background: #ccc;
    border: 1px solid #333;
    border-radius: 10px;
}
</style>