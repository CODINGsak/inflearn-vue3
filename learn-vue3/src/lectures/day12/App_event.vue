<template>
	<div>
		<button @click="printEvent('Hello', $event)">event handler</button>
		<hr />
		<input type="text" @keyup="onKeyUp" />
	</div>
</template>

<script>
export default {
	setup() {
		const printEvent = (message, event) => {
			console.log('message: ', message);
			console.log('event.target: ', event.target);
			console.log('event.target.tagName: ', event.target.tagName);
		};
		const onKeyUp = event => {
			console.log('event.key :', event.key);
		};
		return { printEvent, onKeyUp };
	}
};
</script>

<style lang="scss" scoped></style>
