<script setup>
const msg = 'Hello Vue 3.0';
const styleColor = 'color: green';
</script>

<template>
	<h1>
		{{ msg }}
	</h1>

	<!-- <h2 style="color: blue">Example of inline style</h2> -->
	<h2 :style="styleColor">Example of inline style</h2>
</template>

<style>
h1 {
	color: red;
}
</style>
