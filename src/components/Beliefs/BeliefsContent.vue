<template>
	<div class="beliefs-img pr">
		<slot />
	</div>
	<div class="content-container flex fd-column jc-right pr">
		<div class="company-belief col-6 flex fd-column">
			<p class="flex jc-center">
				{{ contentText }}
			</p>
			<h4 class="flex jc-center">
				{{ moto }}
			</h4>
		</div>
	</div>
</template>

<script>
export default {
	name: "BeliefsContent",
	props: {
		contentText: String,
		moto: String,
	},
};
</script>

<style lang="scss">
@import "/src/assets/styles/variables.scss";
.beliefs-img {
	position: relative;
	margin: 0 auto;
	max-width: 1440px;
}
.company-belief {
	p {
		width: 280px;
		margin-left: 150px;
		margin-bottom: 110px;
	}
	h4 {
		width: 280px;
		margin-left: 150px;
		margin-bottom: 90px;
		position: relative;
		font-size: 1.5em;
		color: $block-text;
	}
	h4::after {
		z-index: 0;
		content: "";
		position: absolute;
		left: 300%;
		top: -110%;
		height: calc(600% + 6px);
		width: 1px;
		background-color: #c1c1c1;
	}
}
@media screen and (max-width: $bp-laptop-s) {
	h4::after {
		display: none;
	}
	.company-belief {
		p {
			margin-bottom: 50px;
		}
	}
}
@media screen and (max-width: $bp-tablet) {
	.company-belief {
		p {
			width: 60%;
			margin-left: 30px;
			margin-bottom: 18px;
		}
		h4 {
			width: 65%;
			justify-content: flex-start;
			margin-top: 55px;
			margin-bottom: 0;
			margin-left: 30px;
			font-size: 1.2em;
			color: $block-text;
		}
	}
}
@media screen and (max-width: $bp-mobile-l) {
	.company-belief {
		p {
			width: 90%;
		}
		h4 {
			width: 90%;
		}
	}
}
</style>
