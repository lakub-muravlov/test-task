<template>
	<section class="beliefs">
		<div class="content-container">
			<h2 class="flex jc-left" id="beliefs">Beliefs</h2>
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

@mixin line-facade {
	content: "";
	position: absolute;
	width: 1px;
	background-color: #c1c1c1;
}

.beliefs {
	background-color: $beliefs-section-bg;
	min-height: 700px;
}
h2 {
	position: relative;
	align-self: flex-start;
	padding-left: 130px;
	padding-top: 70px;
	margin-bottom: 54px;
}
h2::before {
	@include line-facade();
	left: 141.5px;
	top: 0;
	height: 45px;
	background-color: #c1c1c1;
}
h2::after {
	@include line-facade();
	left: 142px;
	top: calc(100% + 20px);
	height: 545px;
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
	h2::before {
		display: none;
	}
	h2::after {
		display: none;
	}
	img {
		width: 45%;
	}
}

@media screen and (max-width: $bp-tablet) {
	h2 {
		justify-content: flex-start;
		padding-left: 30px;
		margin-left: 0px;
		padding-top: 124px;
		margin-bottom: 15px;
	}
}

@media screen and (max-width: 520px) {
	img {
		width: 60%;
		transform: translateY(-308px);
	}
}

@media screen and (max-width: $bp-mobile-l) {
	img {
		width: 90%;
		transform: translateY(-348px);
	}

	h2 {
		font-size: 1.8em;
		padding-top: 184px;
	}
}

@media screen and (max-width: $bp-mobile-m) {
	img {
		transform: translateY(-328px);
	}

	h2 {
		padding-top: 184px;
	}
}

@media screen and (max-width: $bp-mobile-s) {
	img {
		transform: translateY(-288px);
	}

	h2 {
		padding-top: 124px;
	}
}
</style>
