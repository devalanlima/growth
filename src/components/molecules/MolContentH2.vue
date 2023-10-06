<template>
    <div class="wrapper">
        <h2 class="base-title">{{ props.baseTitle }}</h2>
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
    gap: 16px;
}

.base-title {
    text-align: center;
    line-height: 120%;
    margin: 0;
    /* 38.4px */
}

.base-paragraph {
    text-align: center;
}
</style>