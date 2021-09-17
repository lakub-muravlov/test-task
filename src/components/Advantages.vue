<template>
	<section class="advantages content-container">
		<h1>Advantages</h1>
		<h2>Partnership</h2>
		<h2>Professional community</h2>
		<h2>Successful wins</h2>
		<p>
			We make sure projects become successful through strategic partnership and
			guidance
		</p>
		<p>
			At our disposal are top industries professionals who constantly share
			their experience with our partners
		</p>
		<p>
			Our Background is full of successfully deployed projects. We know how to
			lead you to success
		</p>
	</section>
</template>

<script>
export default {
	name: "Advantages",
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.advantages {
	min-height: 550px;
	display: grid;
	justify-content: center;
	grid-gap: 0px 30px;
	grid-template-rows: 250px 100px auto;
	grid-template-columns: calc(100% / 4) calc(100% / 4) calc(100% / 4);
	h1 {
		align-self: center;
		grid-column-start: 1;
		grid-column-end: 4;
	}
	h2 {
		align-self: center;
		position: relative;
	}
	h2::after {
		content: "";
		width: 20%;
		position: absolute;
		left: 0;
		bottom: -50px;
		border-width: 0 0 3px;
		border-style: solid;
	}
	p {
		margin-top: 50px;
		align-self: flex-start;
	}
	margin-bottom: 120px;
}

.row1 {
	grid-column-start: 1;
	grid-column-end: 4;
}

@media only screen and (max-width: $bp-tablet) {
	h1 {
		align-self: center;

		font-size: 1.8em;
	}

	.advantages {
		overflow: hidden;
		display: grid;
		align-content: center;
		grid-template-columns: 260px;
		grid-template-rows: auto;
		grid-row-gap: 40px;

		margin-bottom: 50vw;
	}
}
</style>
