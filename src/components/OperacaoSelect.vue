<script setup>
import { ref } from "vue";

//pegando valor reativo passado

const modelValue = ref("+");
</script>

<template>
	<!-- selecionando operração -->
	<select v-model="modelValue" @change="$emit('update:modelValue', modelValue)">
		<option value="+">+</option>
		<option value="-">-</option>
		<option value="*">*</option>
		<option value="/">/</option>
	</select>
</template>

<style scoped>
select {
	width: 100%;
	padding: 15px;
	font-size: 1.2em;
	border: 2px solid #ddd;
	border-radius: 8px;
	text-align: center;
	margin-bottom: 10px;
	font-family: "Arial", sans-serif;
}

option {
	font-size: 1.1em;
}

select:focus {
	outline: none;
	border-color: #6c5ce7;
}
</style>
