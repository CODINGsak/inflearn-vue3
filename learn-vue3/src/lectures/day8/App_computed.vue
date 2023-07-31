<template>
	<div>
		<h2>{{ teacher.name }}</h2>
		<h3>have a class?</h3>
		<!-- <p>{{ teacher.lectures.length > 0 ? 'yes' : 'no' }}</p> -->
		<p>{{ haslecture }}</p>
		<button v-on:click="counter++">Counter : {{ counter }}</button>
	</div>
</template>

<script>
import { computed, reactive, ref } from 'vue';

export default {
	setup() {
		const teacher = reactive({
			name: 'coding',
			lectures: ['HTML/CSS', 'JAVA', 'Vue3']
		});
		const haslecture = computed(() => {
			return teacher.lectures.length > 0 ? 'yes' : 'no';
		});
		const counter = ref(0);
		return {
			teacher,
			haslecture,
			counter
		};
	}
};
</script>

<style lang="scss" scoped></style>
