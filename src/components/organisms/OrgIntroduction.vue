<template>
    <section class="wrapper">
        <MolContenth1
        base-title="A powerful solution to grow your startup. Fast!"
        base-text="Organise, collaborate, and track progress seamlessly with our one-stop-shop startup growth tool."
        />

        <div class="btn-wrapper">
            <AtomBaseButton
            bnt-name="Get started"
            btn-width="full"
            bg-color="color-one"
            />
            <AtomBaseButton
            :left-icon="IconWebCam"
            bnt-name="Book a demo"
            btn-width="full"
            bg-color="color-two"
            />
        </div>
    </section>
</template>

<script setup lang="ts">
import AtomBaseButton from '../atoms/AtomBaseButton.vue';
import IconWebCam from '../atoms/Icons/IconWebCam.vue';
import MolContenth1 from '../molecules/MolContentH1.vue';
</script>

<style scoped>
.wrapper{
    display: flex;
    flex-direction: column;
    gap: 32px; 
}

.btn-wrapper{
    display: flex;
    flex-direction: column;
    gap: 19px;
}
</style>