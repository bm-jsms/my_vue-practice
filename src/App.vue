<script setup>
const msg = 'Hello Vue 3.0';
const styleColor = 'color: green';
const valid = true;

const fruits = ['🍎', '🍌', '🍇'];

const arrayFruits = [
	{ name: '🍎', quantity: 10, price: 1 },
	{ name: '🍌', quantity: 5, price: 2 },
	{ name: '🍇', quantity: 0, price: 3 },
];

const myObject = {
	name: '🍎',
	quantity: 10,
	price: 1,
};
</script>

<template>
	<h1>
		{{ msg }}
	</h1>

	<!-- <h2 style="color: blue">Example of inline style</h2> -->
	<h2 :style="styleColor">Example of inline style</h2>

	<hr />

	<h2>
		{{ valid ? 'Valid' : 'Not Valid' }}
	</h2>

	<hr />

	<p v-if="valid">Is Valid ⭐</p>
	<p v-else>Is not Valid ❌</p>

	<h2 v-show="valid">Is Valid ⭐</h2>

	<hr />

	<h2>My Fruits</h2>

	<ul>
		<li v-for="(fruit, index) in fruits" :key="index">
			{{ fruit }}
		</li>
	</ul>

	<hr />

	<h3>Test</h3>
	<ul>
		<li v-for="fruit in arrayFruits" :key="fruit.name">
			<span> Name: {{ fruit.name }} </span>
			<span> Quality: {{ fruit.quantity }} </span>
			<span> Price: {{ fruit.price }} </span>
		</li>
	</ul>

	<hr />

	<h2>v-for Object</h2>
	<ul>
		<li v-for="value in myObject" :key="value">
			{{ value }}
		</li>
	</ul>
	<ul>
		<li v-for="(value, key) in myObject" :key="key">{{ key }}: {{ value }}</li>
	</ul>

	<hr />

	<h2>v-if with v-for</h2>
	<ul>
		<template v-for="fruit in arrayFruits">
			<li v-if="fruit.quantity > 0" :key="fruit.name">
				<span> Name: {{ fruit.name }} </span>
				<span> Quality: {{ fruit.quantity }} </span>
				<span> Price: {{ fruit.price }} </span>
			</li>
		</template>
	</ul>
</template>

<style>
h1 {
	color: red;
}
</style>
