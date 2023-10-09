<template>
    <section class="wrapper-content">
        <MolContentH2 
        class="content-h2"
        base-title="Essential tools for propelling your business forward"
        base-text="Streamline your operations, boost productivity and drive growth with our essential tools" 
        />

        <div class="wrapper-down">
            <MolContentH3
            class="content-h3"
            base-title="Dashboard and reporting"
            base-text="Gain valuable insights with real-time monitoring. Track key performance indicators and make data-driven decisions. "
            />
            <ul>
                <li v-for="item in items">
                    <MolAccordion
                    :base-title="item.title"
                    :base-text="item.text"                    
                    :after-icon="IconArrow"
                    />
                </li>
            </ul>
        </div>
    </section>

    <div class="statements-wrapper">
        <img
        class="statements-image"
        src="/statements.png"
        alt="A statement sales graph with de text: 'Statements are automatically generated in PDF by the 10th of each month'"
        >
    </div>
</template>

<script setup lang="ts">
import IconArrow from '../atoms/Icons/IconArrow.vue';
import MolContentH2 from '../molecules/MolContentH2.vue';
import MolContentH3 from '../molecules/MolContentH3.vue';
import MolAccordion from '../molecules/MolAccordion.vue';
import { ref } from "vue";

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

<style scoped>
.wrapper-content{
    display: flex;
    flex-direction: column;
    gap: 40px;
}

.wrapper-down{
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.statements-wrapper{
    overflow: hidden;
}
.statements-image{
    width: 100%;
    height: auto;
    scale: 1.2;
    margin-left: -10px;
}
</style>