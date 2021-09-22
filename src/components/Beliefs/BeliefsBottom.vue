<template>
	<div class="content-container ">
		<div class="offers-grid item-wrapper flex jc-left">
			<slot />
		</div>
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
	overflow: hidden;
	min-height: 160px;

	display: grid;

	grid-gap: 86px 30px;
	grid-template-columns: 360px 360px;
}

.item-wrapper {
	margin-left: 160px;
}

@media screen and (max-width: 920px) {
	.item-wrapper {
		padding-bottom: 40px;
		margin-left: 160px;
	}
	.offers-grid {
		column-gap: 50px;
		grid-template-columns: 250px 250px;
	}
}
@media screen and (max-width: $bp-tablet) {
	.item-wrapper {
		padding-bottom: 40px;
		margin-left: 30px;
	}
	.offers-grid {
		max-width: calc(100vw - 60px);
		overflow: hidden;
		min-height: 160px;
		display: grid;
		margin-top: 40px;
		grid-gap: 30px;
		grid-template-columns: 360px;
	}
}
@media screen and (max-width: $bp-mobile-l) {
	.item-wrapper {
		padding-bottom: 40px;
		padding-top: 30px;
	}
	.offers-grid {
		max-width: calc(100vw - 30px);
		overflow: hidden;
		display: grid;
		margin-top: 0px;
		grid-template-columns: 200px;
		grid-template-rows: auto;
		grid-row-gap: 25px;
	}
}
</style>
