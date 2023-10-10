<template>
    <header class="base-header">
        <OrgBaseNavbar/>
    </header>
    <main class="base-main">
        <div class="wrapper-first">
            <OrgIntroduction/>
            <OrgEssentials/>
        </div>
        <OrgHowItWorks/>
        <div class="wrapper-first">
            <OrgPricing/>
        </div>
    </main>
    <footer>
        
    </footer>
</template>

<script setup lang="ts">
import OrgBaseNavbar from '../organisms/OrgBaseNavbar.vue';
import OrgEssentials from '../organisms/OrgEssentials.vue';
import OrgHowItWorks from '../organisms/OrgHowItWorks.vue';
import OrgIntroduction from '../organisms/OrgIntroduction.vue';
import OrgPricing from '../organisms/OrgPricing.vue';


</script>

<style scoped>

.wrapper-first{
    padding: 0 16px;
    display: flex;
    flex-direction: column;
    gap: 63px;
}
.base-header{
    padding: 24px 16px 0px 16px;
}

.base-main{
    margin-top: 84px;
    display: flex;
    flex-direction: column;
    gap: 63px;
}

</style>