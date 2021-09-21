<template>
	<h2>{{ title }}</h2>
	<p>
		<slot />
	</p>
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
	margin-left: 65px;
	align-self: flex-start;
	justify-self: end;
	position: relative;
}
h2::after {
	content: "";
	width: 25%;
	position: absolute;
	left: 75%;
	bottom: -20px;
	border-width: 0 0 3px;
	border-style: solid;
}

@media screen and (max-width: $bp-tablet) {
	h2 {
		margin-left: 0;
		margin-top: 0%;
		align-self: flex-end;
		justify-self: flex-start;
		position: relative;
	}
	p {
		margin-bottom: 0%;
		align-self: center;
	}
	h2::after {
		content: "";
		width: 25%;
		position: absolute;
		left: 0;
		bottom: -20px;
		border-width: 0 0 3px;
		border-style: solid;
	}
}
</style>
