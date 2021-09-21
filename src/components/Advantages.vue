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

		<AdvantageItem title="Successful wins">
			Our Background is full of successfully deployed projects. We know how to
			lead you to success
		</AdvantageItem>
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
	min-height: 200px;
	padding-top: 70px;
	padding-bottom: 115px;
	display: grid;
	justify-content: center;
	grid-gap: 100px 15px;
	grid-template-rows: auto auto;
	grid-template-columns: calc(100% / 4) calc(100% / 4) calc(100% / 4);
	h1 {
		align-self: center;
		grid-column-start: 1;
		grid-column-end: 4;
	}
}

@media only screen and (max-width: $bp-tablet) {
	h1 {
		align-self: center;
		font-size: 1.8em;
	}

	.advantages {
		display: flex;
		max-width: 90%;
		margin-left: 30px;
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-end;
		h1 {
			align-self: flex-start;
		}
	}
}
@media only screen and (max-width: $bp-mobile-l) {
	h1 {
		margin-top: -75px;
		padding-top: 20px;
		align-self: flex-start;
		font-size: 1.8em;
	}

	.advantages {
		display: flex;
		row-gap: 0px;
		max-width: calc(100% - 30px);
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-end;
		h1 {
			align-self: flex-start;
		}
	}
}
</style>
