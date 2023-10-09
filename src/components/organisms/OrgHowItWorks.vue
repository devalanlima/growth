<template>
    <section class="base-section">
        <MolHowWorksVideo />
        <hr class="base-hr">
        <MolHowWorksComments/>
    </section>
</template>

<script setup lang="ts">
import MolHowWorksComments from "../molecules/MolHowWorksComments.vue";
import MolHowWorksVideo from "../molecules/MolHowWorksVideo.vue";

</script>

<style scoped>
.base-section {
    background-color: var(--color-two);
    padding: 64px 16px;
    display: flex;
    flex-direction: column;
    gap: 64px;
}

.base-hr {
    width: 343px;
    border:1px solid var(--color-five);
}
</style>

