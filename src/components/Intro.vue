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
	background-image: url("../assets/styles/img/intro.png");
	background-position: bottom;
	background-repeat: no-repeat;
	background-size: 100% calc(100vw / 2);
	box-shadow: inset 0 0 0 1000px rgba(72, 88, 141, 0.7);
	height: 700px;
	color: $intro-text;
}

@media screen and (max-width: $bp-laptop-l) {
	.intro {
		background-size: 140%;
	}
}
@media screen and (max-width: $bp-tablet) {
	.intro {
		background-size: auto;
		background-position: center;
	}
}
</style>
