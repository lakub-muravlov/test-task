<template>
	<section class="beliefs">
		<div class="content-container">
			<h1 class="flex jc-left">Beliefs</h1>
		</div>
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
		<!-- </div> -->
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
			moto: "Flexible approach, consistent results",
		};
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.beliefs {
	background-color: $beliefs-section-bg;
	min-height: 700px;
}
h1 {
	position: relative;
	align-self: flex-start;
	padding-left: 130px;
	padding-top: 70px;
	margin-bottom: 54px;
}
h1::before {
	content: "";
	position: absolute;
	left: 141.5px;
	top: 0;
	height: 45px;
	width: 1px;
	background-color: #c1c1c1;
}
h1::after {
	content: "";
	position: absolute;
	left: 142px;
	top: calc(100% + 20px);
	height: 545px;
	width: 1px;
	background-color: #c1c1c1;
}
img {
	z-index: 1;
	max-height: 494px;
	width: 51%;
	right: 0;
	position: absolute;
	overflow: hidden;
	margin-bottom: -35%;
	transform: translateY(-247px);
}
@media screen and (max-width: $bp-laptop-s) {
	h1::before {
		display: none;
	}
	h1::after {
		display: none;
	}
	img {
		max-height: 494px;
		width: 45%;
		right: 0;
		position: absolute;
		overflow: hidden;
		transform: translateY(-247px);
	}
}

@media screen and (max-width: $bp-tablet) {
	h1 {
		justify-content: flex-start;
		padding-left: 30px;
		margin-left: 0px;
		padding-top: 124px;
		margin-bottom: 15px;
	}
}
@media screen and (max-width: 520px) {
	img {
		max-height: 494px;
		width: 60%;
		right: 0;
		position: absolute;
		overflow: hidden;

		transform: translateY(-308px);
	}
}

@media screen and (max-width: $bp-mobile-l) {
	img {
		max-height: 494px;
		width: 90%;
		right: 0;
		position: absolute;
		overflow: hidden;

		transform: translateY(-348px);
	}

	h1 {
		justify-content: flex-start;
		padding-left: 30px;
		font-size: 1.8em;
		margin-left: 0px;
		padding-top: 184px;
		margin-bottom: 15px;
	}
}

@media screen and (max-width: $bp-mobile-m) {
	img {
		max-height: 494px;
		width: 90%;
		right: 0;
		position: absolute;
		overflow: hidden;

		transform: translateY(-328px);
	}

	h1 {
		justify-content: flex-start;
		padding-left: 30px;
		font-size: 1.8em;
		margin-left: 0px;
		padding-top: 184px;
		margin-bottom: 15px;
	}
}

@media screen and (max-width: $bp-mobile-s) {
	img {
		max-height: 494px;
		width: 90%;
		right: 0;
		position: absolute;
		overflow: hidden;

		transform: translateY(-288px);
	}

	h1 {
		justify-content: flex-start;
		padding-left: 30px;
		font-size: 1.8em;
		margin-left: 0px;
		padding-top: 124px;
		margin-bottom: 15px;
	}
}
</style>
