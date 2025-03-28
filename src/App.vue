<script setup>
import { ref } from "vue";
import NumeroInput from "./components/NumeroInput.vue";
import OperacaoSelect from "./components/OperacaoSelect.vue";
import Resultado from "./components/Resultado.vue";

const num1 = ref(0);
const num2 = ref(0);
const operacao = ref("+");
</script>

<template>
	<!-- container mais externo para tentar alinhar tudo no meio        -->
	<main class="main-container">
		<div class="app-container">
			<h1>Calculadora Vue</h1>
			<div class="calc-container">
				<NumeroInput v-model="num1" />
				<OperacaoSelect v-model="operacao" />
				<NumeroInput v-model="num2" />
				<Resultado :num1="num1" :num2="num2" :operacao="operacao" />
			</div>
		</div>
	</main>
</template>

<style scoped>
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: "Arial", sans-serif;
}

.main-container {
	width: 100%;
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #4d66d6;
}

.app-container {
	text-align: center;
	background: linear-gradient(to bottom, #ff9ff3, #6c5ce7);
	border-radius: 15px;
	box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
	padding: 40px;
	width: 100%;
	max-width: 400px;
	box-sizing: border-box;
}

h1 {
	font-size: 2.5em;
	color: #fff;
	margin-bottom: 30px;
}

.calc-container {
	width: 100%;
}

input,
select {
	font-size: 1.2em;
	padding: 15px;
	border-radius: 8px;
	border: 2px solid #ddd;
	margin-bottom: 10px;
	width: 100%;
	text-align: center;
	font-family: "Arial", sans-serif;
}

input:focus,
select:focus {
	outline: none;
	border-color: #6c5ce7;
}

select {
	background-color: #ff9ff3;
}

button {
	padding: 15px;
	width: 100%;
	font-size: 1.2em;
	border: none;
	background-color: #6c5ce7;
	color: white;
	border-radius: 8px;
	cursor: pointer;
}

button:hover {
	background-color: #5d47c0;
}

body {
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
}

html,
body {
	height: 100%;
}
</style>
