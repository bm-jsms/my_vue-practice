<script setup>
const msg = 'Hello Vue 3.0';
const styleColor = 'color: green';
const valid = true;

const fruits = ['🍎', '🍌', '🍇'];
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

	<h2>My Fruits</h2>

	<ul>
		<li v-for="(fruit, index) in fruits" :key="index">
			{{ fruit }}
		</li>
	</ul>
</template>

<style>
h1 {
	color: red;
}
</style>
