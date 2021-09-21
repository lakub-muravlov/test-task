<template>
	<div class="content-container flex fd-column jc-right">
		<div class="company-belief col-6 flex fd-column">
			<p class="flex jc-center">
				{{ contentText }}
			</p>
			<h2 class="flex jc-center">
				{{ moto }}
			</h2>
		</div>
		<slot />
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

.company-belief {
	p {
		margin-left: 20px;
		margin-bottom: 108px;
	}
	h2 {
		margin-left: -20px;
		font-size: 1.5em;
		color: $block-text;
	}
}
@media screen and (max-width: $bp-laptop-s) {
	.company-belief {
		p {
			margin-bottom: 50px;
		}
	}
}
@media screen and (max-width: $bp-tablet) {
	.company-belief {
		p {
			margin-left: 0px;
			margin-bottom: 18px;
		}
		h2 {
			margin-left: 0px;
			font-size: 1.5em;
			color: $block-text;
		}
	}
}
</style>
