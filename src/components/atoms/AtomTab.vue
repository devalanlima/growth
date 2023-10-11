<template>
    <ul class="tab-wrapper">
        <li v-for="(item, index) in props.items" :key="index">
            <label :class="[
                picked === item ? 'tab-btn-selected' : 'tab-btn'
            ]">
                {{ item }}
                <input class="radio-input" type="radio" :value="item" v-model="picked" />
            </label>
        </li>
    </ul>
</template>

<script setup lang="ts">
import { ref, watch, onMounted } from "vue";

const picked = ref<string | null>(null)
watch(()=>picked.value, (newValue: string | null)=>{
    sendPicked(newValue)
})

interface Props {
    items: Array<string>
}
const props = defineProps<Props>()
onMounted(()=>{
    picked.value = props.items[0]
    
})

const emit = defineEmits(['picked'])
const sendPicked = (pickedValue: string | null)=> emit('picked', pickedValue)
</script>

<style scoped>
.tab-wrapper {
    width: fit-content;
    display: flex;
    gap: 4px;
    padding: 8px;
    justify-content: center;
    align-items: center;

    border-radius: 8px;
    background: var(--color-six);
}

.tab-btn,
.tab-btn-selected {
    border-radius: 8px;
    display: flex;
    padding: 8px 16px;
    justify-content: center;
    align-items: center;
    gap: 4px;
    color: var(--color-two);
    font-size: 16px;
    font-weight: 500;
    line-height: 150%;
    /* 24px */
}

.tab-btn-selected {
    color: var(--color-one);
    background-color: var(--color-three);
}

.radio-input {
    width: 0;
    height: 0;
    opacity: 0;
    position: absolute;
    left: -999999999;
    top: -999999999;
    display: none;
}
</style>