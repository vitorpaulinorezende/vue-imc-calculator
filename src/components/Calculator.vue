<template>
	<div class="container">
		<input name="height" id="height" placeholder="altura">
		<input name="weight" id="weight" placeholder="peso">
		<button id="calc" v-on:click="calc()">Calcular</button>
		<p>{{ msg }}</p>
	</div>
</template>

<script>
	export default {
		data: function() {
			return {
				msg: ''
			};
		},
		name: 'Calculator',
		methods: {
			calc() {
				var height = document.querySelector('#height').value;
				var weight = document.querySelector('#weight').value;
				
				height *= height;

				var imc = weight / height;

				if (isNaN(imc)) {
					this.msg = "Precha os Dados Corretamente";
				} else {
					this.msg = imc.toFixed(2);
				}
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.container {
		padding: 20px;
	}
	input {
		margin-right: 20px;
		padding: 10px;
		margin-bottom: 20px;
	}
	button {
		padding: 10px;
	}
</style>
