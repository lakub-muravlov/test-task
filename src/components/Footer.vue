<template>
	<footer>
		<div class="flex fd-row content-container jc-sb ai-center">
			<p>©2021 Test Vetures Inc. All rights reserved</p>
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

@media only screen and (max-width: $bp-tablet) {
	footer {
		div {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
			width: 90%;
			height: 120px;
		}
		p {
			width: 45%;
			margin-top: 30px;
			font-size: 0.6em;
		}
		img {
			width: 30%;
			margin-bottom: 30px;
		}
	}
}
</style>
