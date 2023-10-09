<template>
    <header class="base-header">
        <OrgBaseNavbar/>
    </header>
    <main class="base-main">
        <OrgIntroduction/>
        <OrgEssentials/>
    </main>
    <footer>
        
    </footer>
</template>

<script setup lang="ts">
import OrgBaseNavbar from '../organisms/OrgBaseNavbar.vue';
import OrgEssentials from '../organisms/OrgEssentials.vue';
import OrgIntroduction from '../organisms/OrgIntroduction.vue';


</script>

<style scoped>
.base-header{
    padding: 24px 16px 0px 16px;
}

.base-main{
    margin-top: 84px;
    padding: 0 16px;
    display: flex;
    flex-direction: column;
    gap: 63px;
}

</style>