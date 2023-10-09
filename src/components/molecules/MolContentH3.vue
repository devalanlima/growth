<template>
    <div class="wrapper">
        <h3 class="base-title">{{ props.baseTitle }}</h3>
        <p class="base-paragraph">{{ props.baseText }}</p>
    </div>
</template>

<script setup lang="ts">
interface Props {
    baseTitle: String;
    baseText: String;
}

const props = defineProps<Props>();
</script>

<style scoped>
.wrapper{
    display: flex;
    flex-direction: column;
    gap: 8px;
}
.base-title {
    margin: 0;
    font-size: 24px;
    line-height: 120%; /* 28.8px */
}
</style>