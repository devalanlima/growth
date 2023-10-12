<template>
    <section class="footer-wrapper">
        <IconGrowth class="icon-growth" color="white" />
        <MolCardTextField class="card-textfield" />
        <div class="navigations-wrapper">
            <MolNavigationLinks
                base-title="Company"
                :base-items="companyLinks"
            />
            <MolNavigationLinks
                base-title="Resources"
                :base-items="resourcesLinks"
            />
            <MolNavigationLinks
                base-title="Contact"
                :base-items="contactLinks"
            />
        </div>
        <div class="wrapper-copyright">
            <MolSocials :items="socialLinks" />
            <p class="copyright">© 2023 Growth. All rights reserved</p>
        </div>
    </section>
</template>

<script setup lang="ts">
import IconGrowth from '../atoms/Icons/IconGrowth.vue';
import IconLinkedin from '../atoms/Icons/IconLinkedin.vue';
import IconTwitter from '../atoms/Icons/IconTwitter.vue';
import MolCardTextField from '../molecules/MolCardTextField.vue';
import MolNavigationLinks from '../molecules/MolNavigationLinks.vue';
import MolSocials from '../molecules/MolSocials.vue';

const socialLinks = [
    {
        icon: IconLinkedin,
        link: '#'
    },
    {
        icon: IconTwitter,
        link: '#'
    }
]

const companyLinks = [
    {
        item: 'About',
        link: '#'
    },
    {
        item: 'Our Process',
        link: '#'
    },
    {
        item: 'Join our team',
        link: '#'
    },
]

const resourcesLinks = [
    {
        item: 'About',
        link: '#'
    },
    {
        item: 'Our Process',
        link: '#'
    },
    {
        item: 'Join our team',
        link: '#'
    },
]

const contactLinks = [
    {
        item: 'hello@growthapp.com',
        link: "#"
    }
]

</script>

<style scoped>
.icon-growth{
    margin-bottom: 24px;
}
.card-textfield{
    margin-bottom: 40px;
}
.footer-wrapper {
    background: var(--color-two);
    padding: 64px 16px 24px 16px;
    display: flex;
    flex-direction: column;
}

.navigations-wrapper {
    display: flex;
    gap: 70px;
    row-gap: 42px;
    flex-wrap: wrap;
    margin-bottom: 64px;
}

.wrapper-copyright{
    display: flex;
    flex-direction: column;
    gap: 24px;
}
.copyright {
    color: #BCC2C3;
    font-size: 14px;
    font-weight: 400;
    line-height: 150%;
    /* 21px */
}
</style>