<template>
	<div>
		<button @click="increment">Counter: {{ counter }}</button>
	</div>
</template>

<script>
import { onMounted, ref } from 'vue';

export default {
	setup() {
		const counter = ref(0);
		const increment = () => counter.value++;

		onMounted(() => {
			console.log('success mounted');
		});

		return {
			counter,
			increment
		};
	}
};
</script>

<style lang="scss" scoped></style>
