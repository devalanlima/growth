<template>
    <section class="images-wrapper">
        <img class="tean-image" src="/Tean-capodopera.png" alt="">
        <div class="wrapper-down">
            <img class="sales-image" src="/sales.png" alt="">
            <div class="wrapper-small">
                <img class="woman-image" src="/woman.png" alt="">
                <img class="team-image" src="/team-call.png" alt="">
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.tean-image,
.woman-image,
.team-image {
    width: 100%;
}

.wrapper-down {
    display: grid;
    grid-template-columns: 2fr 1fr;
    align-items: end;
    gap: 19px;
    margin-top: -27px;
} 

.sales-image {
    width: 100%;
    height: auto;
}

.wrapper-small {
    display: flex;
    flex-direction: column;
    gap: 19px;
}

.woman-image,
.team-image {
    width: 100%;
    height: auto;
}</style>

