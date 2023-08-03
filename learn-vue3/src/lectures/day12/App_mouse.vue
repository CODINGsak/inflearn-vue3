<template>
	<div>
		<div id="modifiers">
			<div @click="clickDiv">
				this is div
				<p @click="clickP">
					this is p
					<span @click.stop="clickSpan"> this is span </span>
					<!-- div까지 연결되서 버블성 연속 이벤트 발생인데, stop으로 span만 할수 있다 -->
				</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	setup() {
		const clickDiv = () => {
			console.log('clickDiv');
		};
		const clickP = () => {
			console.log('clickP');
		};
		const clickSpan = () => {
			console.log('clickSpan');
			alert('good!!');
		};

		return {
			clickDiv,
			clickP,
			clickSpan
		};
	}
};
</script>

<style scoped>
#modifiers div,
#modifiers p,
#modifiers span {
	padding: 40px;
}
#modifiers div {
	background-color: greenyellow;
}
#modifiers p {
	background-color: #2fff63;
}
#modifiers span {
	background-color: #9dbb16;
	display: block;
}
</style>
