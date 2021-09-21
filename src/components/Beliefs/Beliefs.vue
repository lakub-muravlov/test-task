<template>
	<section class="beliefs">
		<h1 class="flex jc-left">Beliefs</h1>
		<BeliefsContent :contentText="contentText" :moto="moto">
			<img src="../../assets/img/beliefs.png" alt="" />
		</BeliefsContent>
		<BeliefsBottom>
			<BeliefsItem title="Co-Investing">
				Each and everyone can join us in out vision and put own capital to
				growth in the international market
			</BeliefsItem>
			<BeliefsItem title="Mentoring">
				We have mentoring and advisory expertise to help business owners build a
				successful line of work.
			</BeliefsItem>
		</BeliefsBottom>
	</section>
</template>

<script>
import BeliefsBottom from "./BeliefsBottom.vue";
import BeliefsItem from "./BeliefsItem.vue";
import BeliefsContent from "./BeliefsContent.vue";
export default {
	name: "Beliefs",
	components: {
		BeliefsItem,
		BeliefsBottom,
		BeliefsContent,
	},
	data() {
		return {
			contentText:
				"We believe in teams. Crypto is about constant iteration and being in touch with the community.",
			moto: "Flexible approach,consistent results",
		};
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.beliefs {
	background-color: $beliefs-section-bg;
	min-height: 700px;
	margin-bottom: 120px;
}
h1 {
	align-self: flex-start;
	margin-left: 100px;
	margin-top: 54px;
	margin-bottom: 54px;
}

img {
	width: 43vw;
	max-height: 494px;
	max-width: 720px;
	position: relative;

	margin-bottom: -350px;
	top: -450px;
	left: 700px;
	right: 0;
}
@media screen and (max-width: $bp-laptop-s) {
	img {
		left: 550px;
		margin-bottom: -250px;
	}
}
@media screen and (max-width: $bp-tablet) {
	.beliefs {
		margin-bottom: 120px;
	}

	h1 {
		justify-content: flex-start;
		margin-left: 0px;
		margin-top: 24px;
		margin-bottom: 24px;
	}

	img {
		width: 50vw;
		position: relative;
		margin-bottom: -350vw;
		top: -510px;
		left: 290px;
		right: 0;
	}
}

@media screen and (max-width: $bp-mobile-l) {
	img {
		width: 70vw;
		position: relative;
		margin-bottom: -350vw;
		top: -440px;
		left: 95px;
		right: 0;
	}
}
</style>
