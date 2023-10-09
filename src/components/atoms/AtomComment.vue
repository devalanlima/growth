<template>
    <div class="wrapper-comment">
        <p class="comment">{{ props.comment }}</p>
        <div class="wrapper-infos">
            <p class="user">{{ props.user }}</p>
            <p class="location">{{ props.location }}</p>
        </div>
    </div>
</template>

<script setup lang="ts">
interface Props {
    comment: string;
    user: string;
    location: string;
}

const props = defineProps<Props>()
</script>

<style scoped>
.wrapper-comment {
    display: flex;
    width: full;
    height: fit-content;
    min-width: 204px;
    padding: 32px 24px;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;

    border-radius: 16px;
    background: #FFF;
}

.comment {
    color: var(--color-two);
    font-feature-settings: 'clig' off, 'liga' off;
    font-family: Poppins;
    font-size: 16px;
    font-style: italic;
    font-weight: 400;
    line-height: 150%;
    /* 24px */
}

.user {
    color: var(--color-two);
    font-feature-settings: 'clig' off, 'liga' off;
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 24px */
}

.location {
    color: var(--color-two);
    font-feature-settings: 'clig' off, 'liga' off;
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 24px */
    
}

.wrapper-infos{
    display: flex;
    flex-direction: column;
    align-items: baseline;
}
</style>