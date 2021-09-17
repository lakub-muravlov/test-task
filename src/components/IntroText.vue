<template>
	<section class="content-container flex fd-column jc-right">
		<div class="company-motto col-6 flex fd-column">
			<h1 class="flex jc-center">Crypto Capital <br />for Success</h1>
			<p class="flex jc-center">
				We believe that every investement<br />
				we make has the potential to expand<br />
				and build our future
			</p>
		</div>
		<div class="learn-more flex col-4 jc-left">
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
//y 572 x 372
@import "/src/assets/styles/variables.scss";
p {
	font-size: 1.1em;
}
.company-motto {
	h1 {
		color: $intro-text;
		margin-top: 54px;
		margin-bottom: 54px;
	}
	p {
		color: $intro-text;
		margin-left: 20px;
		margin-bottom: 108px;
	}
}
.learn-more {
	margin-left: 92px;
	div {
		border: 1px solid white;
		height: 48px;
	}
	button {
		width: 172px;
		height: 48px;
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
</style>
