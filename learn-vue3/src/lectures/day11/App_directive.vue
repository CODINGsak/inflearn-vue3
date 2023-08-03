<template>
	<div>
		<p v-text="msg"></p>
		<p>{{ msg }}</p>
		<p>{{ htmlmsg }}</p>
		<p v-html="htmlmsg"></p>
		<p v-once>{{ msg }} !!!!</p>
		<!-- cant modify F12 v-once -->
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		const msg = ref('hello');
		const htmlmsg = ref('<strong>v-html!!</strong>');
		return {
			msg,
			htmlmsg
		};
	}
};
</script>

<style lang="scss" scoped></style>
