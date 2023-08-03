<template>
	<div v-memo="[subscriber]">
		<p>subscriber : {{ subscriber }}</p>
		<p>view: {{ view }}</p>
		<p>like : {{ like }}</p>
	</div>
	<button @click="subscriber++">Subscribe ++</button>
	<button @click="view++">View ++</button>
	<button @click="like++">Like ++</button>
	<div>
		<p>subscriber : {{ subscriber }}</p>
		<p>view: {{ view }}</p>
		<p>like : {{ like }}</p>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		const subscriber = ref(4000);
		const view = ref(400);
		const like = ref(2);
		return {
			subscriber,
			view,
			like
		};
	}
};
</script>

<style lang="scss" scoped></style>
