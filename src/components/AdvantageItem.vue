<template>
	<div>
		<h2>{{ title }}</h2>
		<p>
			<slot />
		</p>
	</div>
</template>

<script>
export default {
	name: "AdvantageItem",
	props: {
		title: String,
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

h2 {
	align-self: flex-end;
	position: relative;
	padding-bottom: 80px;
}
h2::after {
	content: "";
	width: 40px;
	position: absolute;
	left: 0;
	bottom: 40px;
	border-width: 0 0 3px;
	border-style: solid;
}
p {
	font-size: 0.8em;
	margin-top: 0px;
	width: 80%;
	margin-bottom: 20px;
	align-self: flex-start;
}
@media only screen and (max-width: $bp-mobile-l) {
	h2 {
		margin-top: 30px;
		padding-bottom: 60px;
		align-self: flex-start;
	}
	h2::after {
		bottom: 30px;
	}
	p {
		width: 80%;
		margin-top: 0px;
		margin-bottom: 30px;
		align-self: flex-start;
	}
}
</style>
