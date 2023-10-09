<template>
    <div class="wrapper-all">
        <div class="wrapper-mol">
            <MolContentH3
            :base-title="props.baseTitle"
            :base-text="props.baseText"
            />
            <AtomLearnMore />
        </div>
        <img
        class="image"
        :src="props.urlImage"
        :alt="props.altImage"
        >
    </div>
</template>

<script setup lang="ts">
import AtomLearnMore from '../atoms/AtomLearnMore.vue';
import MolContentH3 from '../molecules/MolContentH3.vue';

interface Props {
    baseTitle: string;
    baseText: string;
    urlImage: string;
    altImage: string;
}

const props = defineProps<Props>()
</script>

<style scoped>
.wrapper-all{
    display: flex;
    flex-direction: column;
    gap: 24px;
}
.wrapper-mol {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
</style>
