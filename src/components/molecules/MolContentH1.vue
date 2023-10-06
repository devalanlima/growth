<template>
    <div class="wrapper">
        <h1 class="base-title">{{ props.baseTitle }}</h1>
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
    margin: 0;
}

.base-paragraph {
    color: var(--color-two);
    text-align: center;
    font-size: 18px;
    line-height: 160%;
    /* 28.8px */
}
</style>