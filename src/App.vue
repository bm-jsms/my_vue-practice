<script setup>
const msg = 'Hello Vue 3.0';
const styleColor = 'color: green';
const valid = true;
</script>

<template>
	<h1>
		{{ msg }}
	</h1>

	<!-- <h2 style="color: blue">Example of inline style</h2> -->
	<h2 :style="styleColor">Example of inline style</h2>

	<h2>
		{{ valid ? 'Valid' : 'Not Valid' }}
	</h2>
	<p v-if="valid">Is Valid ⭐</p>
	<p v-else>Is not Valid ❌</p>

	<h2 v-show="valid">Is Valid ⭐</h2>
</template>

<style>
h1 {
	color: red;
}
</style>
