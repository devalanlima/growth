<template>
    <div class="wrapper">
        <h2 class="base-h2">Don't just take our word for it, see the success  stories from businesses just like yours.</h2>
        <div class="caroussel">
            <AtomComment
            v-for="(item, key) in items"
            :key="key"
            :comment="item.comment"
            :user="item.user"
            :location="item.location"
            />
        </div>
    </div>
</template>

<script setup lang="ts">
import AtomComment from '../atoms/AtomComment.vue';
import { ref } from "vue";

const items = ref([
    {
        comment: "“Our business has seen a significant increase in productivity since we started using the Growth app.”",
        user: "Katherine Smith",
        location: "Capodopera",
    },
    {
        comment: "“As a small business owner, it's important to have a tool that can help me keep track of everything. The Growth app has been a lifesaver for me, allowing me to manage my contacts, schedule appointments, and track progress all in one place.”",
        user: "Jonathan Lee",
        location: "Red Bolt",
    },
    {
        comment: "“The dashboards and reporting feature has provided valuable insights into our performance and helped us make data-driven decisions. It's a game changer for us.”",
        user: "David Wilson",
        location: "Slide",
    },
    {
        comment: "“Our business has seen a significant increase in productivity since we started using the Growth app.”",
        user: "Katherine Smith",
        location: "Capodopera",
    },
])

</script>

<style scoped>
.wrapper{
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.base-h2{
    color: #fff;
}

.caroussel{
    display: flex;
    flex-direction: column;
    width: 100%;
    overflow-x: auto;
    gap: 32px;
}
</style>