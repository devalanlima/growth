<template>
    <div class="card-wrapper">
        <div class="text-wrapper">
            <p class="base-title">Subscribe to newsletter</p>
            <p class="base-text">Subscribe now to receive tips on how to take your business to the next level.</p>
        </div>
        <div class="inputs-wrapper">
            <AtomTextField
                input-type="email"
                input-placeholder="Enter your email"
                @action="getValue"
            />
            <AtomButtonSmall
                class="base-btn"
                bnt-name="Subscribe"
                bg-color="color-one"
                btn-width="padding"
            />
        </div>
    </div>
</template>

<script setup lang="ts">
import AtomButtonSmall from '../atoms/AtomButtonSmall.vue';
import AtomTextField from '../atoms/AtomTextField.vue';

const getValue = (e: string) => {
    console.log(e);

}
</script>

<style scoped>
.card-wrapper {
    display: flex;
    padding: 24px;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;

    border-radius: 16px;
    background: #F4F4F6;
}

.text-wrapper {
    display: flex;
    flex-direction: column;
}

.inputs-wrapper {
    display: flex;
    gap: 8px;
}

.base-title {
    color: var(--color-five);
    font-family: Poppins;
    font-size: 18px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;
    /* 27px */
}

.base-text {
    color: #131316;
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 24px */
}</style>