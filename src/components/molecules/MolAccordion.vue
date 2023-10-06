<template>
    <div 
    :class="['info-wrapper',{
        'selected': isOpen
    }]"
    >
        <button class="title-wrapper" @click="isOpen = !isOpen">
            <h4 class="title">{{ props.baseTitle }}</h4>
            <component 
            v-if="isOpen"
            :is="props.afterIcon"
            />
            <component
            v-else
            :is="props.beforeIcon"
            />
        </button>
        <p v-if="isOpen">{{ props.baseText }}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const isOpen = ref<boolean>(false)

interface Props {
    baseTitle: String,
    baseText: String,
    beforeIcon?: Object,
    afterIcon?: Object,
}

const props = defineProps<Props>()


</script>

<style scoped>
.info-wrapper {
    display: flex;
    flex-direction: column;
    gap: 8px;
    border-bottom: 1px solid var(--color-seven);
    padding: 16px 0;
}

.selected{
    border-bottom: 1px solid var(--color-two);
}

.title-wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}
</style>