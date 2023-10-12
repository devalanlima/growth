<template>
    <input
        class="base-input"
        :placeholder="props.inputPlaceholder"
        :type="props.inputType"
        v-model="inputValue"
        @input="emit('action', inputValue)"
    >
</template>

<script setup lang="ts">
import { ref } from "vue";

interface Props {
    inputType: 'text' | 'email' | 'search';
    inputPlaceholder: string
}

const props = defineProps<Props>()

const inputValue = ref<string | null>(null)

const emit = defineEmits(['action'])

</script>

<style scoped>
.base-input {
    padding: 12px;
    align-items: center;
    border-radius: 8px;
    border: 1px solid #BEBDC6;
    width: 100%;
}

.base-input::placeholder {
    color: var(--color-five);
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 24px */
}
</style>