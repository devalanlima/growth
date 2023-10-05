<template>
    <h2 
    :class="props.textColor === 'color-one'?'base-title-one': 'base-title-two'"
    >
        {{ props.baseTitle }}
    </h2>
</template>

<script setup lang="ts">
interface Props {
    textColor: 'color-one' | 'color-two';
    baseTitle: String;
}

const props = defineProps<Props>()
</script>

<style scoped>
.base-title-one, .base-title-two {
    font-feature-settings: 'clig' off, 'liga' off;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    line-height: 110%;    /* 39.6px */
}

.base-title-one {
    color: var(--color-one);
}

.base-title-two {
    color: var(--color-two);
}
</style>