<template>
	<div :style="styleObject">
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, culpa
		ratione? Laborum beatae provident, obcaecati voluptate harum velit. Officiis
		iusto nemo totam eligendi iure inventore natus aliquid veritatis recusandae
		iste!
	</div>
</template>

<script>
import { reactive } from 'vue';

export default {
	setup() {
		const styleObject = reactive({
			color: 'red',
			fontSize: '13px'
		});
		return {
			styleObject
		};
	}
};
</script>

<style lang="scss" scoped></style>
