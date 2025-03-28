<script setup>
import { computed } from "vue";

//pegando propriedades para colocar de resultado
const props = defineProps(["num1", "num2", "operacao"]);

const resultado = computed(() => {
	const n1 = parseFloat(props.num1) || 0;
	const n2 = parseFloat(props.num2) || 0;

	switch (props.operacao) {
		case "+":
			return n1 + n2;
		case "-":
			return n1 - n2;
		case "*":
			return n1 * n2;
		case "/":
			return n2 !== 0 ? n1 / n2 : "Erro";
		default:
			return 0;
	}
});
</script>

<template>
	<p class="resultado">Resultado: {{ resultado }}</p>
</template>

<style scoped>
.resultado {
	font-size: 1.5em;
	text-align: center;
	margin-top: 20px;
	font-family: "Arial", sans-serif;
	color: #333;
	font-weight: bold;
}
</style>
