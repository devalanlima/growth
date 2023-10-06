<template>
	<PageMain />
</template>

<script setup lang="ts">
import PageMain from './components/pages/PageMain.vue';
</script>

<style>
:root {
	--font-Poppins: 'Poppins', sans-serif;
	--color-one: #fff;
	--color-two: #131316;
	--color-three: #4891FF;
	--color-four: #DAF4FE;
	--color-five: #494A4D;
	--color-six: #F5F5F5;
	--color-seven: #DFDEE2
}

h1,
h2,
h3 {
	color: var(--color-two);
	font-feature-settings: 'clig' off, 'liga' off;
	font-family: Poppins;
	font-style: normal;
	font-weight: 500;
	margin: 0;
	padding: 0;
}

h1 {
	font-size: 36px;
	line-height: 110%;
	/* 39.6px */
}

h2 {
	font-size: 32px;
	line-height: 120%;
	/* 38.4px */
}

h3 {
	font-size: 24px;
	line-height: 120%;
	/* 28.8px */
}

h4 {
	font-size: 20px;
	font-weight: 400;
	line-height: 120%; /* 24px */
}

p {
	color: var(--color-five);
	font-family: Poppins;
	font-size: 16px;
	font-style: normal;
	font-weight: 400;
	line-height: 160%;
	margin: 0;
	/* 25.6px */
}
</style>
