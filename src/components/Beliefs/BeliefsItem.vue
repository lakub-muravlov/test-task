<template>
	<div class="flex beliefs-item cg-30">
		<div class="">
			<h3>{{ title }}</h3>
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

h3 {
	white-space: nowrap;
	margin-left: 0px;
	align-self: flex-start;
	justify-self: end;
	position: relative;
}

h3::after {
	content: "";
	width: 40px;
	position: absolute;
	right: 0;
	bottom: -20px;
	border-width: 0 0 2px;
	border-style: solid;
}

p {
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
	h3::after {
		left: 0;
	}
}
@media screen and (max-width: $bp-tablet) {
	.beliefs-item {
		row-gap: 40px;
	}
}

@media screen and (max-width: $bp-mobile-l) {
	h3 {
		margin-left: 30px;
		margin-top: 0;
		justify-self: flex-start;
		position: relative;
	}
	p {
		margin-left: 30px;
		justify-self: flex-start;
	}
	h3::after {
		width: 25%;
	}
}
</style>
