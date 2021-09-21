<template>
	<div class="offers-grid">
		<slot />
	</div>
</template>

<script>
export default {
	name: "BeliefsBottom",
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.offers-grid {
	z-index: 10;
	overflow: hidden;
	height: 160px;
	display: grid;
	justify-content: center;
	margin-left: -140px;
	grid-gap: 0px 10px;
	grid-template-columns: 300px 240px 300px 240px;
}

@media screen and (max-width: $bp-tablet) {
	.offers-grid {
		overflow: hidden;
		min-height: 35vh;
		display: grid;
		margin-left: 5%;
		margin-top: 300px;
		grid-template-columns: 260px;
		grid-template-rows: auto;
		grid-row-gap: 20px;
	}
}
@media screen and (max-width: $bp-mobile-l) {
	.offers-grid {
		overflow: hidden;
		min-height: 54vh;
		display: grid;
		margin-left: 5%;
		margin-top: 315px;
		grid-template-columns: 260px;
		grid-template-rows: auto;
		grid-row-gap: 25px;
	}
}
</style>
