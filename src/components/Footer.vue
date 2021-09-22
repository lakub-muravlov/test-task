<template>
	<footer>
		<div class="flex fd-row content-container jc-sb ai-center">
			<p>©2021 Test Vetures Inc. All rights reserved</p>
			<img src="../assets/img/logo-footer.svg" alt="" />
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
	background-color: white;
	bottom: 0;
	left: 0;
	right: 0;
	width: 100%;
	div {
		height: 120px;
		p {
			margin-left: 140px;
			font-size: 0.6em;
		}
	}
}

@media only screen and (max-width: $bp-tablet) {
	footer {
		div {
			p {
				width: 150px;
				margin-left: 30px;
			}
		}
	}
}

@media only screen and (max-width: $bp-mobile-l) {
	footer {
		div {
			display: flex;
			flex-direction: column;
			justify-content: flex-start;
			align-items: flex-start;
			width: 90%;
			height: 205px;
			margin-left: 30px;
			p {
				margin-left: 0px;
				margin-top: 35px;
				margin-bottom: 55px;
				width: 135px;
				margin-top: 30px;
				font-size: 0.6em;
			}
		}

		img {
			width: 175px;
		}
	}
}
</style>
