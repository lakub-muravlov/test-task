<template>
	<section class="advantages content-container" id="advantages">
		<h1>Advantages</h1>
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

.advantages {
	padding-left: 0px;
	min-height: 200px;
	padding-top: 70px;
	padding-bottom: 90px;
	display: grid;
	justify-content: center;
	grid-gap: 100px 15px;
	grid-template-rows: auto auto;
	grid-template-columns: calc(100% / 4) calc(100% / 4) calc(100% / 4);
	h1 {
		position: relative;
		grid-column-start: 1;
		grid-column-end: 4;
	}
	h1::before {
		content: "";
		position: absolute;
		left: 4px;
		bottom: -110%;
		height: 55px;
		width: 1px;
		background-color: #c1c1c1;
	}
	h1::after {
		content: "";
		position: absolute;
		left: 4px;
		top: -110%;
		height: 45px;
		width: 1px;
		background-color: #c1c1c1;
	}
}

.right-line {
	position: relative;
}
.right-line::before {
	content: "";
	position: absolute;
	left: calc(-205.3% - 10px);
	top: 100%;
	height: 91px;
	width: 1.5px;
	background-color: #c1c1c1;
}

.right-line::after {
	content: "";
	position: absolute;
	right: -40px;
	top: -130%;
	height: 280%;
	width: 1px;
	background-color: #c1c1c1;
}

@media only screen and (max-width: $bp-laptop-s) {
	.right-line::after {
		display: none;
	}
	.right-line::before {
		display: none;
	}
	h1::before {
		display: none;
	}
	h1::after {
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
		h1 {
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

		display: flex;
		max-width: calc(100% - 60px);
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-end;
		h1 {
			margin-top: -75px;
			padding-top: 20px;
			margin-left: 0px;

			align-self: flex-start;
			font-size: 1.8em;
		}
		h1::before {
			z-index: -1;
			display: inline;
			content: "";
			position: absolute;
			left: 0px;
			top: 5px;
			height: calc(300vw + 10px);
			width: 1px;
			background-color: #c1c1c1;
		}
	}
}
</style>
