<template>
    <nav>
        <ul class="base-navbar">
            <li>
                <a href="">
                    <IconGrowth/>
                </a>
            </li>

            <li class="relative">
                <AtomDropdownButton 
                v-if="width < 768" 
                @action="showMenu" 
                />

                <MolNavigationList 
                class="navigation-list" 
                v-if="width >= 768 || isOpen" 
                />
            </li>
        </ul>
    </nav>
</template>

<script setup lang="ts">
import AtomDropdownButton from '../atoms/AtomDropdownButton.vue';
import IconGrowth from '../atoms/Icons/IconGrowth.vue';
import MolNavigationList from '../molecules/MolNavigationList.vue';
import { useWindowSize } from '@vueuse/core'
import { ref, watch } from 'vue'
const { width } = useWindowSize()

const isOpen = ref<boolean>(false)

const showMenu = () => {
    if (isOpen.value) {
        isOpen.value = false
    } else {
        isOpen.value = true
    }
}

watch(width, (newValue) => {
    if (newValue >= 768) {
        isOpen.value = false
    }
})
</script>

<style scoped>
.base-navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1248px;
    margin: auto;
}

@media (max-width: 768px) {
    .navigation-list {
        position: absolute;
        right: 0;
    }
}
</style>