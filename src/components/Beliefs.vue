<template>
	<section class="beliefs ">
		<div class="content-container flex fd-column jc-right">
			<div class="company-belief col-6 flex fd-column">
				<h1 class="flex jc-center">Beliefs</h1>
				<p class="flex jc-center">
					We believe in teams. Crypto is about <br />
					constant iteration and being in touch <br />
					with the community.
				</p>
				<h2 class="flex jc-center">
					Flexible approach, <br />
					consistent results
				</h2>
				<img src="../assets/styles/img/beliefs.png" alt="" />
			</div>
		</div>
		<div class="offers-grid">
			<h2>
				Co-Investing
			</h2>
			<p>
				Each and everyone can join us in out vision and put own capital to
				growth in the international market
			</p>
			<h2>Mentoring</h2>
			<p>
				We have mentoring and advisory expertise to help business owners build a
				successful line of work.
			</p>
		</div>
	</section>
</template>

<script>
export default {
	name: "Beliefs",
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

.beliefs {
	z-index: 5;
	background-color: $beliefs-section-bg;
	min-height: 700px;
	margin-bottom: 120px;
}

.company-belief {
	h1 {
		align-self: flex-start;
		margin-left: 100px;
		margin-top: 54px;
		margin-bottom: 54px;
	}
	p {
		margin-left: 20px;
		margin-bottom: 108px;
	}
	h2 {
		margin-left: -20px;
		font-size: 1.5em;
		color: $block-text;
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
}

.offers-grid {
	z-index: 10;
	overflow: hidden;
	height: 160px;
	display: grid;
	justify-content: center;
	margin-left: -140px;
	grid-gap: 0px 10px;
	grid-template-columns: 300px 240px 300px 240px;
	h2 {
		margin-left: 65px;
		align-self: flex-start;
		justify-self: end;
		position: relative;
	}
	h2::after {
		content: "";
		width: 25%;
		position: absolute;
		left: 75%;
		bottom: -20px;
		border-width: 0 0 3px;
		border-style: solid;
	}
}

@media screen and (max-width: $bp-laptop-s) {
	.company-belief {
		img {
			left: 550px;
			margin-bottom: -250px;
		}
		p {
			margin-bottom: 50px;
		}
	}
}
@media screen and (max-width: $bp-tablet) {
	.beliefs {
		margin-bottom: 120px;
	}
	.company-belief {
		h1 {
			justify-content: flex-start;
			margin-left: 0px;
			margin-top: 24px;
			margin-bottom: 24px;
		}
		p {
			margin-left: 0px;
			margin-bottom: 18px;
		}
		h2 {
			margin-left: 0px;
			font-size: 1.5em;
			color: $block-text;
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
	.offers-grid {
		overflow: hidden;
		min-height: 80vh;
		display: grid;
		margin-left: 5%;
		margin-top: 80vh;
		grid-template-columns: 260px;
		grid-template-rows: auto;
		grid-row-gap: 20px;

		h2 {
			margin-left: 0;
			align-self: flex-end;
			justify-self: flex-start;
			position: relative;
		}
		p {
			align-self: center;
		}
		h2::after {
			content: "";
			width: 25%;
			position: absolute;
			left: 0;
			bottom: -20px;
			border-width: 0 0 3px;
			border-style: solid;
		}
	}
}

@media screen and (max-width: $bp-mobile-l) {
	.company-belief {
		img {
			width: 70vw;
			position: relative;
			margin-bottom: -350vw;
			top: -440px;
			left: 95px;
			right: 0;
		}
	}
}
</style>
