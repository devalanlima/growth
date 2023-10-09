<template>
    <section class="wrapper-content">
        <MolContentH2 class="content-h2" base-title="Essential tools for propelling your business forward"
            base-text="Streamline your operations, boost productivity and drive growth with our essential tools" />

        <MolDashboardAndReporting/>

        <MolAdvantajes 
        v-for="item in items"
        :key="item.title"
        :base-title="item.title"
        :base-text="item.text"
        :url-image="item.urlImage" 
        :alt-image="item.altImage" 
        />
    </section>
</template>

<script setup lang="ts">
import MolContentH2 from '../molecules/MolContentH2.vue';
import MolAdvantajes from '../molecules/MolAdvantajes.vue';
import MolDashboardAndReporting from '../molecules/MolDashboardAndReporting.vue';
import { ref } from "vue";

const items = ref([
    {
        title: 'Business communications',
        text: 'Keep track of your contacts, schedule appointments and never miss a follow-up with our powerful contact management solution. Store and organise contact information for clients, partners, and potential investors.',
        urlImage: '/business-communications_small.png',
        altImage: 'picture of a woman holding a video conference'
    },
    {
        title: 'Communication tools',
        text: 'Keep your team informed and on the same page with our real-time communication tools for messaging, video conferencing and more.',
        urlImage: '/messages_small.png',
        altImage: 'message app'
    },
    {
        title: 'Boost productivity and efficiency',
        text: 'Organize, delegate and keep track of tasks with our easy-to-use task management system. Create and manage to-do lists and tasks, and assign them to team members.',
        urlImage: '/todolist_small.png',
        altImage: 'to do list app'
    }
])

</script>

<style scoped>
.wrapper-content {
    display: flex;
    flex-direction: column;
    gap: 40px;
}

.wrapper-down {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.statements-wrapper {
    overflow: hidden;
}

.statements-image {
    width: 100%;
    height: auto;
    scale: 1.2;
    margin-left: -10px;
}
</style>