<template>
    <section class="questions-wrapper">
        <h2 class="base-h2">Frequently asked questions</h2>
        <MolAskedQuestions/>
    </section>
</template>

<script setup lang="ts">
import MolAskedQuestions from '../molecules/MolAskedQuestions.vue';


</script>

<style scoped>
.questions-wrapper{
    display: flex;
    flex-direction: column;
    gap: 32px;
}
.base-h2{
    text-align: center;
}
</style>