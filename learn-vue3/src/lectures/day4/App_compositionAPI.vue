<template>
	<div>
		<h2>reactive</h2>
		<p>{{ reactiveMessage }}</p>
		<button v-on:click="addMessage">Add +!</button>
		<h2>normal</h2>
		<p>{{ normalMessage }}</p>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
		const reactiveMessage = ref('Hello reactive');
		const addMessage = () => {
			reactiveMessage.value = reactiveMessage.value + '!';
		};
		const normalMessage = 'hello normal';

		return {
			reactiveMessage,
			normalMessage,
			addMessage
		};
	}
};
</script>

<style lang="scss" scoped></style>
