<template>
    <section class="questions-wrapper">
        <AtomTab
        @picked="tabValue"
        :items="questionThemes"
        />
        <ul>
            <li>
                <MolAccordion v-for="(question, key) in atualQuestions" :key="key" :base-title="question.question"
                    :base-text="question.answer" :before-icon="IconPlus" :after-icon="IconX" />
            </li>
        </ul>
    </section>
</template>

<script setup lang="ts">
import AtomTab from "../atoms/AtomTab.vue";
import IconPlus from "../atoms/Icons/IconPlus.vue";
import IconX from "../atoms/Icons/IconX.vue";
import MolAccordion from "./MolAccordion.vue";
import { ref, onMounted } from "vue";

const questionThemes = ref<Array<string>>([
    'All', 
    'Getting Started',
    'Pricing',
])

const atualQuestions = ref()

const tabValue = (e: string) => {
    switch (e) {
        case 'All':
            atualQuestions.value = allQuestions.value
            break;
        case 'Getting Started':
            atualQuestions.value = gettingStartedQuestions.value
            break;
        case 'Pricing':
            atualQuestions.value = pricingQuestions.value
        break;
        default:
            break;
    }
}

onMounted(()=>{
    tabValue(questionThemes.value[0])
})

const allQuestions = ref([
    {
        question: "How does the contact management feature help me keep track of clients and partners?",
        answer: "You can track contacts and analyze data."
    },
    {
        question: "Can I customize the dashboards and reporting feature to display the metrics that are most important to my business?",
        answer: "Yes, you can customize your dashboards."
    },
    {
        question: "How does the task management feature help me delegate tasks to my team and track progress?",
        answer: "Efficiently delegate and track tasks."
    },
    {
        question: "Can I collaborate with my team in real-time using all tools?",
        answer: "Real-time collaboration with various tools."
    },
    {
        question: "Is the app available on all devices?",
        answer: "Accessible on all devices."
    },
    {
        question: "How does the app help me stay compliant when working with freelancers and contractors?",
        answer: "Manage compliance with freelancers and contractors."
    },
])

const gettingStartedQuestions = ref([
    {
        question: "How do I get started with our service?",
        answer: "To get started, simply sign up for an account on our website and follow the onboarding process. It's quick and easy!"
    },
    {
        question: "What are the basic features I should know about when starting?",
        answer: "Our basic features include contact management, task delegation, and real-time collaboration. These are great starting points."
    },
    {
        question: "Is there a tutorial or user guide available for new users?",
        answer: "Yes, we provide a comprehensive user guide and tutorial videos to help you get started and make the most of our service."
    },
    {
        question: "Can I invite team members to join me from the beginning?",
        answer: "Absolutely! You can invite your team members to join your workspace during the onboarding process or later."
    },
    {
        question: "What type of support is available if I encounter any issues during setup?",
        answer: "Our support team is ready to assist you. You can reach out via email or our live chat support for quick help."
    },
    {
        question: "Are there any tips for a smooth start with our service?",
        answer: "Start by setting up your contact list and defining your key tasks. Don't hesitate to explore features and reach out for support."
    },
])

const pricingQuestions = ref([
    {
        question: "How does your pricing model work?",
        answer: "Our pricing is based on a subscription model. We offer different pricing tiers with varying features and usage limits to cater to your specific needs."
    },
    {
        question: "What are the available subscription plans?",
        answer: "We offer three subscription plans: Basic, Pro, and Premium. Each plan comes with different pricing and features, allowing you to choose the one that best suits your requirements."
    },
    {
        question: "Is there a free trial available before committing to a subscription?",
        answer: "Yes, we offer a 14-day free trial for all our subscription plans. It's a great way to test our service and see if it's the right fit for your needs."
    },
    {
        question: "Can I upgrade or downgrade my subscription at any time?",
        answer: "Absolutely! You can upgrade or downgrade your subscription plan at any time to match your changing needs. Your account settings provide an easy way to make these adjustments."
    },
    {
        question: "Are there any discounts available for long-term commitments?",
        answer: "Yes, we offer discounts for annual subscriptions. When you choose to pay for a full year upfront, you can enjoy significant savings compared to the monthly billing option."
    },
    {
        question: "Do you offer refunds if I'm not satisfied with the service?",
        answer: "We have a satisfaction guarantee policy. If you're not completely satisfied with our service within the first 30 days of your subscription, we'll provide a full refund, no questions asked."
    },
])

</script>

<style scoped>
.questions-wrapper{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 40px;
}
</style>