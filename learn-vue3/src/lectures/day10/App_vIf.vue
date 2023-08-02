<template>
	<div>
		<h2 v-if="visible">Hello v-if</h2>
		<h2 v-else>this is false v-else</h2>
		<button v-on:click="visible = !visible">if-else button</button>
		<hr />
		<button v-on:click="type = 'A'">Button A</button>
		<button v-on:click="type = 'B'">Button B</button>
		<button v-on:click="type = 'C'">Button C</button>
		<button v-on:click="type = 'D'">Button D</button>

		<h2 v-if="type === 'A'">this is A</h2>
		<h2 v-else-if="type === 'B'">this is B</h2>
		<h2 v-else-if="type === 'C'">this is C</h2>
		<h2 v-else>this is not A,B,C</h2>
		<hr />
		<template v-if="visible">
			<h1>Title</h1>
			<p>paragraph 1</p>
			<p>paragraph 2</p>
		</template>
		<hr />
		<h1 v-show="okay">v-show practice</h1>
		<button v-on:click="okay = !okay">v-show button</button>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		const visible = ref(true);
		const type = ref('A');
		const okay = ref(true);
		return {
			visible,
			type,
			okay
		};
	}
};
</script>

<style lang="scss" scoped></style>
