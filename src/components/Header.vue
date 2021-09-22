<template>
	<header class="header flex fd-row jc-sb ai-center content-container">
		<div class="col-5">
			<img src="../assets/img/logo-header.svg" alt="" />
		</div>

		<ul class="nav-ul" :class="{ show: showMenu }">
			<li>
				<a href="#advanatages">Advantages</a>
			</li>
			<li>
				<a href="#beliefs">Beliefs</a>
			</li>
			<li>
				<a href="">Insights</a>
			</li>
			<li>
				<a href="" class="submit-application">Submit application</a>
			</li>
		</ul>
		<div class="button" :class="{ show: showMenu }" v-on:click="toggleFunc()">
			<div class="bar1"></div>
			<div class="bar2"></div>
			<div class="bar3"></div>
		</div>
		<nav class="navbar flex ai-center jc-right">
			<a href="#advanatages">Advantages</a>
			<a href="#beliefs">Beliefs</a>
			<a href="">Insights</a>
			<div class="line">
				<a href="" class="submit-application">Submit application</a>
			</div>
		</nav>
	</header>
</template>

<script>
export default {
	name: "Header",

	methods: {
		toggleFunc() {
			this.showMenu = !this.showMenu;
			console.log(this.showMenu);
		},
	},
	data() {
		return {
			showMenu: false,
		};
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";

@mixin startPosition {
	width: 35px;
	height: 5px;
	background-color: #fff;
	margin: 6px 0;
	transition: 0.4s;
}

.button {
	display: none;
	float: right;
	cursor: pointer;
	.bar1 {
		@include startPosition;
		transform: rotate(180deg) translate(0px, 0px);
	}
	.bar2 {
		@include startPosition;
		opacity: 1;
	}
	.bar3 {
		@include startPosition;
		transform: rotate(-180deg) translate(0px, 0px);
	}
}

.button.show {
	.bar1 {
		transform: rotate(-45deg) translate(-9px, 6px);
	}
	.bar2 {
		opacity: 0;
	}
	.bar3 {
		transform: rotate(45deg) translate(-8px, -8px);
	}
}

.nav-ul {
	display: none;
}

.header {
	height: 120px;
}

img {
	margin-left: 160px;
}

.navbar {
	width: 50%;
}

.navbar:nth-child(3) {
	margin-right: 10px;
}

a {
	margin-left: 25px;
	margin-right: 20px;
	font-size: 0.8em;
	white-space: nowrap;
	color: $intro-text;
	text-decoration: none;
	position: relative;
}

a::before {
	content: "";
	position: absolute;
	width: 100%;
	height: 2px;
	top: 23px;
	bottom: 0;
	left: 0;
	background-color: #fff;
	transform: scaleX(0);
	transition: transform 0.3s ease;
}

a:hover::before {
	transform: scaleX(1);
}

.submit-application::before {
	width: 110%;
}

.submit-application::after {
	content: "";
	width: 110%;
	position: absolute;
	left: 0;
	bottom: -5px;
	border-width: 0 0 2px;
	border-style: solid;
}

.submit-application:after:hover::before {
	transform: scaleX(1);
}

.line {
	position: relative;
}

.line::before {
	content: "";
	position: absolute;
	left: 0px;
	top: -250%;
	height: 880px;
	width: 1px;
	background-color: #fff;
}

@media only screen and (max-width: $bp-laptop-s) {
	.navbar {
		display: none;
	}
	.submit-application::after {
		width: 100%;
	}
	.button {
		display: block;
		z-index: 20;

		margin-right: 20px;
	}
	.nav-ul {
		z-index: 19;
		display: inline-block;
		position: fixed;
		left: 0;
		margin: 0;
		padding: 0;
		background-color: $heading-text;
		top: -300px;
		list-style-type: none;
		transition: 1500ms;

		li {
			height: 40px;
			margin-top: 15px;
			text-align: center;
			width: 100vw;
			&:nth-last-child(n) {
				margin-bottom: 10px;
			}
		}
	}
	.nav-ul.show {
		top: 0;
	}
	img {
		margin-left: 160px;
	}
}

@media only screen and (max-width: $bp-tablet) {
	.navbar {
		display: none;
	}
	.submit-application::after {
		width: 100%;
	}
	.button {
		display: block;
		z-index: 20;
		margin-right: 20px;
	}
	.nav-ul {
		z-index: 19;
		display: inline-block;
		position: fixed;
		left: 0;
		margin: 0;
		padding: 0;
		background-color: $heading-text;
		top: -300px;
		list-style-type: none;
		transition: 1500ms;

		li {
			height: 40px;
			margin-top: 15px;
			text-align: center;
			width: 100vw;
			&:nth-last-child(n) {
				margin-bottom: 10px;
			}
		}
	}
	.nav-ul.show {
		top: 0;
	}
	img {
		margin-left: 30px;
	}
	.line::before {
		display: none;
	}
}
</style>
