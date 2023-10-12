<template>
  <div>
    <ul class="wrapper-content">
      <li class="base-title">{{ props.baseTitle }}</li>
      <template v-for="item in props.baseItems">
        <li class="base-text">
          <a :href="item.link">{{ item.item }}</a>
        </li>
      </template>
    </ul>
  </div>
</template>

<script setup lang="ts">
interface BaseItems {
  item: string;
  link: string;
}

interface Props {
  baseTitle: string;
  baseItems: Array<BaseItems>;
}

const props = defineProps<Props>()
</script>

<style scoped>
ul {
  color: white;
}

.wrapper-content {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.base-title {
  color: var(--color-six);
  font-size: 18px;
  font-weight: 600;
  line-height: 120%;
  margin-bottom: 4px;
  /* 21.6px */
}

.base-text {
  color: var(--color-seven);
  font-family: Poppins;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 150%;
  /* 24px */
}
</style>