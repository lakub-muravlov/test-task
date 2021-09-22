<template>
	<div class="flex intro">
		<div class="content-container">
			<slot />
		</div>
	</div>
</template>

<script>
export default {
	name: "Intro",
	components: {},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.intro {
	margin: 0 auto;
	overflow: hidden;
	background-image: url("../assets/img/intro.png");
	background-size: cover;
	background-position: center;
	box-shadow: inset 0 0 0 1000px rgba(72, 88, 141, 0.7);
	min-height: 500px;
	color: $intro-text;
}

@media only screen and (max-width: $bp-mobile-s) {
	.intro {
		background-size: 1300px auto;
		max-height: 570px;
	}
}
</style>
