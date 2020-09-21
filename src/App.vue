<template>
	<div id="app">
		<Calculator />
	</div>
</template>

<script>
	import Calculator from './components/Calculator.vue'

	export default {
		name: 'App',
		components: {
			Calculator
		}
	}
</script>

<style>
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
		font-family: sans-serif;
	}
</style>
