<template>
    <section class="pricing-wrapper" :style="cardColor">
        <div>
            <h3 class="base-h3" :style="contentColor">{{ props.baseTitle }}</h3>
            <p class="base-paragraph" :style="contentColor">{{ props.baseParagraph }}</p>
        </div>

        <div :class="['free-wrapper',
        props.cardColor === 'var(--color-two)'? 'color-white': 'color-black'
        ]">
            <slot/>
        </div>

        <hr :style="contentColor">
        <div :class="['list-wrapper',
        props.cardColor === 'var(--color-two)'? 'color-white': 'color-black'
        ]">
            <slot name="plusList"/>
            <MolList
            :list-color="props.cardColor === 'var(--color-two)' ? 'var(--color-six)' : 'var(--color-two)'"
            :items="props.itemsList"
            />
        </div>

        <AtomBaseButton btn-width="full" bnt-name="Get started" bg-color="color-one" />
    </section>
</template>

<script setup lang="ts">
import AtomBaseButton from '../atoms/AtomBaseButton.vue';
import MolList from './MolList.vue';
import { computed } from "vue";

interface Props {
    cardColor?: 'var(--color-six)' | 'var(--color-two)',
    baseTitle: string;
    baseParagraph: string;
    itemsList: Array<string>;
}

const props = withDefaults(defineProps<Props>(), {
    cardColor: 'var(--color-two)'
})

const cardColor = computed(() => {
    if (props.cardColor === 'var(--color-two)') {
        return ({
            backgroundColor: 'var(--color-two)'
        })
    } else {
        return ({
            backgroundColor: 'var(--color-six)'
        })
    }
})

const contentColor = computed(() => {
    if (props.cardColor === 'var(--color-two)') {
        return ({
            color: 'var(--color-six)'
        })
    } else {
        return ({
            color: 'var(--color-two)'
        })
    }
})

</script>

<style scoped>
.pricing-wrapper {
    display: flex;
    flex-direction: column;
    gap: 32px;
    background: var(--color-six);
    padding: 40px 24px;
    border-radius: 16px;
}

.mol-content-h3-28px {
    gap: 0px;
}

.free-wrapper {
    display: flex;
    gap: 16px;
}

.color-white {
    color: var(--color-six);
}

.color-black {
    color: var(--color-two);
}

.base-h3 {
    font-feature-settings: 'clig' off, 'liga' off;
    font-family: Poppins;
    font-size: 28px;
    font-style: normal;
    font-weight: 500;
    line-height: 120%;
    /* 33.6px */
    letter-spacing: -0.28px;
}

.list-wrapper{
    display: flex;
    flex-direction: column;
    gap: 12px;
}
</style>
