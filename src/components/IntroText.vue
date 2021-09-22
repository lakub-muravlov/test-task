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
p {
	font-size: 1.1em;
}

.company-motto {
	h1 {
		position: relative;
		color: $intro-text;
		width: 80%;
		margin-left: 130px;
		margin-top: 54px;
		margin-bottom: 54px;
	}
	h1::before {
		content: "";
		position: absolute;
		left: 0px;
		bottom: calc(100% + 30px);
		height: 180px;
		width: 1px;
		background-color: #fff;
	}
	h1::after {
		content: "";
		position: absolute;
		left: 0px;
		top: calc(100% + 30px);
		height: 150px;
		width: 1px;
		background-color: #fff;
	}
	p {
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
		margin-left: 140px;
		margin-bottom: 80px;
		font-size: 0.8em;
		font-weight: 700;
		background-color: transparent;
		border-left: 1px solid white;
		border-top: 1px solid white;
		border-bottom: 1px solid white;
		border-right: none;
		color: $intro-text;
	}
	button:hover {
		color: black;
		background-color: #fff;
		transition: 700ms;
	}
	button::after {
		content: "";
		position: absolute;
		left: 0px;
		top: calc(100% + 30px);
		height: 140px;
		width: 1px;
		background-color: #fff;
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
			color: $intro-text;
			width: 80%;
			margin-left: 30px;
			margin-top: 35px;
			margin-bottom: 20px;
		}
		p {
			color: $intro-text;
			width: 45%;
			margin-left: 30px;
			margin-bottom: 38px;
		}
	}
	.learn-more {
		margin-left: 0px;
		div {
			border: 1px solid white;
			height: 48px;
		}
		button {
			width: 172px;
			height: 48px;
			margin-left: 30px;
			font-size: 0.8em;
			font-weight: 700;
			background-color: transparent;
			border-left: 1px solid white;
			border-top: 1px solid white;
			border-bottom: 1px solid white;
			border-right: none;
			color: $intro-text;
		}
		button:hover {
			color: black;
			background-color: #fff;
			transition: 700ms;
		}
	}
}

@media only screen and (max-width: $bp-mobile-l) {
	h1 {
		color: $intro-text;
		font-size: 2.3em;
		width: 80%;
		margin-top: 0px;
		margin-left: 30px;
		margin-bottom: 15px;
	}
	.company-motto {
		p {
			color: $intro-text;
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
