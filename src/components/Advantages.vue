<template>
	<section class="advantages content-container" id="advantages">
		<h2 id="advanatages">Advantages</h2>
		<AdvantageItem title="Partnership">
			We make sure projects become successful through strategic partnership and
			guidance
		</AdvantageItem>

		<AdvantageItem title="Professional community">
			At our disposal are top industries professionals who constantly share
			their experience with our partners
		</AdvantageItem>

		<div class="right-line">
			<AdvantageItem title="Successful wins">
				Our Background is full of successfully deployed projects. We know how to
				lead you to success
			</AdvantageItem>
		</div>
	</section>
</template>

<script>
import AdvantageItem from "@/components/AdvantageItem";
export default {
	name: "Advantages",
	components: {
		AdvantageItem,
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

@mixin line-facade {
	content: "";
	position: absolute;
	background-color: #c1c1c1;
}

.advantages {
	min-height: 200px;
	padding-top: 70px;
	padding-bottom: 90px;
	padding-left: 0px;
	display: grid;
	justify-content: center;
	grid-gap: 100px 15px;
	grid-template-rows: auto auto;
	grid-template-columns: calc(100% / 4) calc(100% / 4) calc(100% / 4);
	h2 {
		position: relative;
		grid-column-start: 1;
		grid-column-end: 4;
	}
	h2::before {
		@include line-facade();
		left: 4px;
		bottom: -110%;
		height: 55px;
		width: 1px;
	}
	h2::after {
		@include line-facade();
		left: 4px;
		top: -110%;
		height: 45px;
		width: 1px;
	}
}

.right-line {
	position: relative;
}

.right-line::before {
	@include line-facade();
	left: calc(-205.3% - 10px);
	top: calc(100% + 11px);
	height: 80px;
	width: 1.5px;
}

.right-line::after {
	@include line-facade();
	right: -40px;
	top: -130%;
	height: 280%;
	width: 1px;
}

@media only screen and (max-width: $bp-laptop-s) {
	.right-line::after {
		display: none;
	}
	.right-line::before {
		display: none;
	}
	h2::before {
		display: none;
	}
	h2::after {
		display: none;
	}
}

@media only screen and (max-width: $bp-tablet) {
	.advantages {
		padding-left: 20%;
		margin-left: -5%;
		display: flex;
		row-gap: 0px;
		max-width: calc(100%);
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-end;
		h2 {
			margin-top: -75px;
			padding-top: 20px;
			margin-left: 0px;
			align-self: flex-start;
			font-size: 1.8em;
		}
	}
}

@media only screen and (max-width: $bp-mobile-l) {
	.advantages {
		padding-left: 0px;
		margin-left: 30px;
		max-width: calc(100% - 30px);
		h2::before {
			z-index: -1;
			display: inline;
			@include line-facade();
			left: 0px;
			top: 5px;
			height: calc(300vw + 10px);
			width: 1px;
		}
	}
}
</style>
