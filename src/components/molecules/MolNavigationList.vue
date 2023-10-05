<template>
    <nav>
        <ul class="items-wrapper">
            <li>
                <AtomBaseButton class="btn-login" bnt-name="Log in" bg-color="color-two" btn-width="full" />
            </li>
            <li v-for="item in items" :key="item">
                <a href="">
                    <span class="horizontal-line"></span>
                    <p class="items">{{ item }}</p>
                </a>
            </li>
        </ul>
    </nav>
</template>

<script setup lang="ts">
import AtomBaseButton from '../atoms/AtomBaseButton.vue';

const items = ['Blog', 'About us', 'Features']
</script>

<style scoped>
.items-wrapper {
    --gap: 25px;
    display: flex;
    flex-direction: column;
    gap: var(--gap);
    margin: auto;
    margin-right: 10px;
    margin-top: 10px;
    padding: 15px 10px 25px 10px;
    background-color: var(--color-six);
    text-align: end;
    border-radius: 16px;
    width: 200px;
}

.items {
    padding-right: 0px;
    color: var(--color-two);
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 150%;  /* 24px */
    position: relative;
    width: fit-content;
    margin: auto;
    margin-right: 25px;
}

.items:hover::after{
    content: '';
    display: block;
    position: absolute;
    left: 0;
    width: 100%;
    height: 2px;
    background-color: var(--color-two);
}

.btn-login {
    padding: 12px 24px;
    border: 1px solid var(--color-five);
}

.horizontal-line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--color-five);
    opacity: .3;
    margin-bottom: var(--gap);
}


@media (min-width: 768px) {
    .items-wrapper {
        display: flex;
        flex-direction: row-reverse;
        margin: 0px;
        padding: 0px;
        padding-right: 20px;
        background: none;
        text-align: end;
        border-radius: 16px;
        width: 100%;
        gap: 40px;
        align-items: center;
    }

    .horizontal-line {
        display: none;
    }

    .btn-login {
        border: none;
    }

    .items{
        margin: 0;
        margin-right: 0px;
    }

}
</style>