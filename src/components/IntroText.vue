<template>
	<section class="content-container flex fd-column jc-right">
		<div class="company-motto col-6 flex fd-column">
			<h1 class="flex jc-right">Crypto Capital for Success</h1>
			<p class="flex jc-center">
				We believe that every investement we make has the potential to expand
				and build our future
			</p>
		</div>
		<div class="learn-more flex jc-left">
			<button>
				Learn more
			</button>
			<div>
				<svg viewbox="0 0 48 48" width="48px" height="48px" class="path">
					<path d="M19 14 L29 24 L19 34" fill="none" stroke="white"></path>
				</svg>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "IntroText",
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";
@mixin line-facade {
	content: "";
	position: absolute;
	width: 1px;
	background-color: #fff;
}
.company-motto {
	h1 {
		position: relative;
		color: $intro-text;
		width: 80%;
		margin: 54px 0 54px 130px;
	}
	h1::before {
		@include line-facade();
		left: 0px;
		bottom: calc(100% + 30px);
		height: 180px;
	}
	h1::after {
		@include line-facade();
		left: 0px;
		top: calc(100% + 30px);
		height: 150px;
	}
	p {
		font-weight: 700;
		font-size: 1.1em;
		width: 60%;
		color: $intro-text;
		margin-left: 165px;
		margin-bottom: 78px;
	}
}
.learn-more {
	div {
		border: 1px solid white;
		height: 48px;
	}
	button {
		position: relative;
		width: 172px;
		height: 48px;
		margin: 0 0 80px 140px;
		font-size: 0.8em;
		font-weight: 700;
		background-color: transparent;
		border-left: 1px solid white;
		border-top: 1px solid white;
		border-bottom: 1px solid white;
		border-right: none;
		border-color: white;
		color: $intro-text;
	}
	button:hover {
		color: black;
		background-color: #fff;
		transition: 700ms;
	}
	button::after {
		@include line-facade();
		left: 0px;
		top: calc(100% + 30px);
		height: 140px;
	}
}

@media only screen and (max-width: $bp-laptop-s) {
	h1::before {
		display: none;
	}
	h1::after {
		display: none;
	}
	button::after {
		display: none;
	}
}

@media only screen and (max-width: $bp-tablet) {
	.company-motto {
		h1 {
			margin: 35px 0 20px 30px;
		}
		p {
			width: 45%;
			margin-left: 30px;
			margin-bottom: 38px;
		}
	}
	.learn-more {
		margin-left: 0px;
		button {
			margin-left: 30px;
		}
	}
}

@media only screen and (max-width: $bp-mobile-l) {
	.company-motto {
		h1 {
			font-size: 2.3em;
			margin-top: 0px;
			margin-left: 30px;
			margin-bottom: 15px;
		}
		p {
			width: 80%;
			margin-left: 30px;
			margin-bottom: 65px;
		}
	}
	.learn-more {
		button {
			margin-left: 30px;
			margin-bottom: 30px;
		}
	}
}
</style>
