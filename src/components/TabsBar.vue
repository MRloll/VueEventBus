<template lang="pug">
.tabs
    ul
        li
            button(@click="evntBusTrigger('Tab 1 payload (A)')") button A
        li
            button(@click="evntBusTrigger('Tab 2 payload (B)')") button B
        li
            button(@click="evntBusTrigger('Tab 3 payload (C)')") button C
</template>

<script>
import { EventBus } from "../main";

export default {
    methods: {
        evntBusTrigger(payload) {
            // sending the event with eventBus and passing payload to it
            //  the data passed could be anything like api response or whatever
            EventBus.$emit("sendPayloadWithEventBus", payload);
        },
    },
};
</script>

<style lang="scss" scoped>
.tabs {
    ul {
        list-style: none;
        li {
            display: inline;
            button {
                background: white;
                border-radius: 10px;
                padding: 10px;
                border: 1px solid #ccc;
                margin: 0 10px;
                cursor: pointer;
            }
        }
    }
}
</style>