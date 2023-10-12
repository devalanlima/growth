<template>
  <button
    :class="[
      props.bgColor === 'color-one' ? 'base-button-one' : 'base-button-two',
      props.btnWidth === 'full' ? 'width-full' : 'width-padding'
    ]"
    @click="action"
  >
    <component :is="props.leftIcon" />
    {{ props.bntName }}
    <component :is="props.rightIcon" />
  </button>
</template>

<script setup lang="ts">

interface Props {
  bgColor: 'color-one' | 'color-two';
  bntName: String;
  btnWidth: 'full' | 'padding';
  leftIcon?: Object;
  rightIcon?: Object;
}
const props = defineProps<Props>()


const emit = defineEmits(['action'])
const action = () => emit('action')

</script>

<style scoped>
.base-button-one,
.base-button-two {
  display: inline-flex;
  padding: 12px 20px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 8px;

  font-family: Poppins;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 150%;
  /* 24px */
  transition: scale 100ms ease-in-out;
}

.base-button-one:hover,
.base-button-two:hover {
  scale: 1.05;
}

.base-button-one {
  background: var(--color-three);
  color: var(--color-one);
}

.base-button-two {
  background: var(--color-six);
  color: var(--color-two)
}

.width-full {
  width: 100%;
}

.width-padding {
  width: fit-content;
}
</style>