<template>
    <div class="wrapper-video">
        <h2 class="base-h2">See how it works and get started in less than 2 minutes</h2>
        <iframe class="base-iframe" src="https://www.youtube.com/embed/IMxDeACOWCE?si=BeYvsjtMMKNt5aXy"
            title="YouTube video player" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen>
        </iframe>
        <AtomBaseButton bnt-name="Get started" btn-width="full" bg-color="color-one" />
    </div>
</template>

<script setup lang="ts">
import AtomBaseButton from '../atoms/AtomBaseButton.vue';

</script>

<style scoped>
.wrapper-video{
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.base-h2 {
    color: var(--color-one);
    text-align: center;
}

.base-iframe {
    width: 343px;
    height: 190px;
    flex-shrink: 0;
    border-radius: 20px;
}
</style>