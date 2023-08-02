<template>
	<div>
		<ul>
			<h1>v-for&v-if! id number 2 or 4</h1>
			<template v-for="(item, index) in items" :key="item.id">
				<li v-if="item.id % 2 === 0">
					ID: {{ item.id }}INDEX : {{ index }},{{ item.message }}
				</li>
			</template>
		</ul>
		<hr />
		<ul>
			<li v-for="(value, key, index) in myObject" :key="key">
				{{ index }}-{{ key }}-{{ value }}
			</li>
		</ul>
	</div>
</template>

<script>
import { reactive } from 'vue';
export default {
	setup() {
		const items = reactive([
			{ id: 1, message: 'JAVA' },
			{ id: 2, message: 'Html' },
			{ id: 3, message: 'Css' },
			{ id: 4, message: 'Script' }
		]);
		const myObject = reactive({
			title: 'title',
			authoe: 'kim',
			price: '10000'
		});
		return {
			items,
			myObject
		};
	}
};
</script>

<style lang="scss" scoped></style>
