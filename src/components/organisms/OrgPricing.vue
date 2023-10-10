<template>
    <section class="princing-wrapper">
        <MolContentH2 
        class="mol-content-h2" 
        base-title="Pricing" 
        base-text="Start free and scale while you grow.
No hidden fees. Unlimited users for free." 
        />

        <div class="cards-wrapper">
            <MolPricingCard
            card-color="var(--color-six)"
            :items-list="freeListItems"
            base-title="Simple"
            base-paragraph="Keep track of your contacts, gain valuable insights, analyse live data and performance metrics.">
                <div class="free-wrapper-slot">
                    <h3 class="free-h3">Free</h3>
                    <p class="free-paragraph">* No credit card required </p>
                </div>
            </MolPricingCard>

            <MolPricingCard
            card-color="var(--color-two)" :items-list="premiumListItems" base-title="Premium"
            base-paragraph="Keep track of your contacts, gain valuable insights, analyse live data and performance metrics.">
                <div class="price-wrapper-slot">
                    <h3 class="price-h3">$49</h3>
                    <p class="price-paragraph">/month</p>
                </div>
                <template #plusList>
                    <p class="price-paragraph">Everything from the free plan plus:</p>
                </template>
            </MolPricingCard>

            <div class="view-features-wrapper">
                <p>All prices are in USD and charged per month with applicable taxes added at checkout.</p>
                <button class="view-features-btn">View features <span class="view-features-arrow"><IconArrow/></span></button>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import IconArrow from '../atoms/Icons/IconArrow.vue';
import MolContentH2 from '../molecules/MolContentH2.vue';
import MolPricingCard from '../molecules/MolPricingCard.vue';

const freeListItems = [
    'Real-time monitoring',
    'Track key performance indicators',
    'Schedule appointments',
    'Organize, delegate and keep track of tasks'
]

const premiumListItems = [
    'Data-driven decisions',
    'Data visualisation',
    'Schedule appointments',
    'Store and organise contact information',
    'Teal-time communication tools for messaging and video conferencing'
]


</script>

<style scoped>
.princing-wrapper{
    display: flex;
    flex-direction: column;
    gap: 40px;
}

.cards-wrapper{
    display: flex;
    flex-direction: column;
    gap: 32px;
}
.mol-content-h2 {
    white-space: pre-wrap;
}

.free-wrapper-slot {
    display: flex;
    gap: 17px;
    align-items: center;
}

.free-h3 {
    font-size: 28px;
    line-height: 120%;
    /* 33.6px */
    letter-spacing: -0.28px;
}

.free-paragraph {
    font-size: 12px;
    line-height: 120%;
    /* 14.4px */
}

.price-wrapper-slot {
    display: flex;
    gap: 2px;
    align-items: end;
}

.price-h3 {
    font-size: 28px;
    font-weight: 500;
    line-height: 120%;
    /* 33.6px */
    letter-spacing: -0.28px;
}

.price-paragraph {
    font-size: 16px;
    font-weight: 400;
    line-height: 120%;
    /* 19.2px */
    letter-spacing: -0.16px;
    padding-right: 30px;
}

.view-features-wrapper{
    display: flex;
    flex-direction: column;
    gap: 16px;
    text-align: center;
}

.view-features-btn{
    display: flex;
    justify-content: center;
    gap: 8px;

    color: var(--color-two);
    font-size: 16px;
    font-weight: 600;
    line-height: 150%; /* 24px */
}

.view-features-arrow{
    transform: rotate(90deg);
}
</style>