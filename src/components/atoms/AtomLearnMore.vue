<template>
    <button class="base-button">
        Learn more <span>
            <IconArrow />
        </span>
    </button>
</template>

<script setup lang="ts">
import IconArrow from './Icons/IconArrow.vue';


</script>

<style scoped>
.base-button {
    color: var(--color-two);
    font-family: Poppins;
    font-size: 16px;
    font-weight: 500;
    line-height: normal;
    letter-spacing: -0.32px;

    display: flex;
    align-items: center;
    gap: 8px;
}
</style>