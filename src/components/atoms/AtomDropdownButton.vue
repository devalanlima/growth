<template>
    <button 
    class="dropdown-button"
    @click="action"
    >
        <div class="line"></div>
        <div class="line"></div>
    </button>
</template>

<script setup lang="ts">
const emit = defineEmits(['action'])

const action = ()=> emit('action')
</script>

<style scoped>
.dropdown-button {
    width: 40px;
    height: 40px;
    flex-shrink: 0;
    border-radius: 12px;
    background: var(--color-six);
    position: relative;
    display: flex;
    gap: 4px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.line{
    display: block;
    width: 20px;
    height: 2px;
    background-color: black;
    position: relative;
}
</style>