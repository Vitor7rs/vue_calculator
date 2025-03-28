<script setup>
import { ref } from "vue";

//pegando valor reativo passado

const modelValue = ref(0);
</script>

<template>
	<input
		type="number"
		v-model="modelValue"
		@input="$emit('update:modelValue', modelValue)"
	/>
</template>

<style scoped>
input {
	width: 100%;
	padding: 15px;
	font-size: 1.2em;
	border: 2px solid #ddd;
	border-radius: 8px;
	text-align: center;
	margin-bottom: 10px;
	font-family: "Arial", sans-serif;
}

input:focus {
	outline: none;
	border-color: #6c5ce7;
}
</style>
