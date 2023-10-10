<template>
    <ul class="base-ul">
        <li 
        class="base-li"
        v-for="(item, index) in props.items"
        :key="index"
        >
            <IconCheck 
            :icon-color="props.listColor"
            />
            <p class="base-paragraph" :style="listColor">{{ item }}</p>
        </li>
    </ul>
</template>

<script setup lang="ts">
import IconCheck from '../atoms/Icons/IconCheck.vue';
import { computed } from "vue";

interface Props {
    items: Array<String>;
    listColor: string;
}

const props = defineProps<Props>()

const listColor = computed(()=>({
    color: props.listColor
}))

</script>

<style scoped>
.base-ul{
    display: flex;
    flex-direction: column;
    gap: 12px;
}
.base-li {
    display: flex;
    gap: 12px;
    align-items: center;
}

.base-paragraph {
    font-size: 16px;
    line-height: 160%;
    /* 25.6px */
}
</style>