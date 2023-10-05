<template>
    <p class="paragraph">{{ props.paragraph }}</p>
</template>

<script setup lang="ts">
interface Props {
    paragraph: String
}
const props = defineProps<Props>()
</script>

<style scoped>
.paragraph {
    color: var(--color-five);
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%; /* 25.6px */
}
</style>