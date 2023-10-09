<template>
    <div class="wrapper-down">
            <MolContentH3 class="content-h3" base-title="Dashboard and reporting"
                base-text="Gain valuable insights with real-time monitoring. Track key performance indicators and make data-driven decisions. " />
            <ul>
                <li v-for="item in items">
                    <MolAccordion :base-title="item.title" :base-text="item.text" :after-icon="IconArrow" />
                </li>
            </ul>
        </div>

        <div class="statements-wrapper">
            <img class="statements-image" src="/statements_small.png"
                alt="A statement sales graph with de text: 'Statements are automatically generated in PDF by the 10th of each month'">
        </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import IconArrow from "../atoms/Icons/IconArrow.vue";
import MolAccordion from '../molecules/MolAccordion.vue';
import MolContentH3 from "./MolContentH3.vue";

const items = ref([
    {
        title: "Real-time monitoring",
        text: "View live data and performance metrics."
    },
    {
        title: "Data visualization",
        text: "have real-time data visualization"
    },
    {
        title: "Alerts and notifications",
        text: "Don't miss anything with our notification center"
    },
])

</script>