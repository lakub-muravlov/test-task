<template>
	<footer>
		<div class="flex fd-row content-container jc-sb ai-center">
			<p>©2021 Test. All rights reserved</p>
			<img src="../assets/styles/img/logo-footer.svg" alt="" />
		</div>
	</footer>
</template>

<script>
export default {
	name: "Footer",
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

footer {
	position: fixed;
	background-color: white;
	bottom: 0;
	width: 100%;
	div {
		height: 120px;
	}
}
p {
	font-size: 0.6em;
}
</style>
