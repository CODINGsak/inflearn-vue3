<template>
	<div>
		<p>{{ message }}</p>
		<p v-once>{{ message }}</p>
		<button @click="message = message + '!'">click ++</button>
		<p v-html="rawHtml"></p>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		const message = ref('hello vue3');
		const rawHtml = ref('<strong>this is v-html</strong>');
		return {
			message,
			rawHtml
		};
	}
};
</script>

<style lang="scss" scoped></style>
