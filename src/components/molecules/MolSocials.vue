<template>
  <ul class="social-wrapper">
    <li
      v-for="(item, index) in props.items"
      :key="index"
    >
      <a :href="item.link">
        <component :is="item.icon" />
      </a>
    </li>
  </ul>
</template>

<script setup lang="ts">
interface IconLink {
  icon: object;
  link: string
}

interface Props {
  items: Array<IconLink>
}

const props = defineProps<Props>()

</script>

<style scoped>
.social-wrapper {
  display: flex;
  gap: 16px;
}
</style>