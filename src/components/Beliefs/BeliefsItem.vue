<template>
	<div class="flex beliefs-item cg-30">
		<div class="">
			<h2>{{ title }}</h2>
		</div>
		<p>
			<slot />
		</p>
	</div>
</template>

<script>
export default {
	name: "BeliefsItem",
	props: {
		title: String,
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

h2 {
	white-space: nowrap;
	margin-left: 0px;
	align-self: flex-start;
	justify-self: end;
	position: relative;
}
h2::after {
	content: "";
	width: 40px;
	position: absolute;
	right: 0;
	bottom: -20px;
	border-width: 0 0 2px;
	border-style: solid;
}
p {
	font-size: 0.8em;
	width: 200px;
}
@media screen and (max-width: 920px) {
	.beliefs-item {
		flex-direction: column;
		justify-content: space-between;
		row-gap: 30px;
	}
	p {
		width: 100%;
	}
	h2::after {
		left: 0;
	}
}
@media screen and (max-width: $bp-tablet) {
	h2::after {
		content: "";
		width: 40px;
		position: absolute;
		left: 0;
		bottom: -20px;
		border-width: 0 0 2px;
		border-style: solid;
	}
	.beliefs-item {
		flex-direction: column;
		row-gap: 40px;
	}
}

@media screen and (max-width: $bp-mobile-l) {
	.beliefs-item {
		flex-direction: column;
		row-gap: 40px;
	}
	h2 {
		margin-left: 30px;
		margin-top: 0%;
		justify-self: flex-start;
		position: relative;
	}
	p {
		margin-left: 40px;

		justify-self: flex-start;
	}
	h2::after {
		content: "";
		width: 25%;
		position: absolute;
		left: 0;
		bottom: -20px;
		border-width: 0 0 2px;
		border-style: solid;
	}
}
</style>
