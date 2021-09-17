<template>
	<header class="header flex fd-row jc-sb ai-center content-container">
		<div class="col-5">
			<img src="../assets/styles/img/logo-header.svg" alt="" />
		</div>

		<ul class="nav-ul" id="nav-ul">
			<li>
				<a href="">Advantages</a>
			</li>
			<li>
				<a href="">Beliefs</a>
			</li>
			<li>
				<a href="">Insights</a>
			</li>
			<li>
				<a href="" class="submit-application">Submit application</a>
			</li>
		</ul>
		<div class="button" id="burger" v-on:click="toggleFunc()">
			<div class="bar1"></div>
			<div class="bar2"></div>
			<div class="bar3"></div>
		</div>
		<nav class="navbar flex ai-center jc-right col-7">
			<a href="">Advantages</a>
			<a href="">Beliefs</a>
			<a href="">Insights</a>
			<a href="" class="submit-application">Submit application</a>
		</nav>
	</header>
</template>

<script>
export default {
	name: "Header",
	methods: {
		toggleFunc() {
			let counter = 0;
			if (counter % 2 === 0) {
				document.getElementById("nav-ul").style.top = "0";
				counter++;
			} else document.getElementById("nav-ul").style.top = "-200";
		},
	},
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";
.button {
	display: none;
	float: right;
	cursor: pointer;
}

.bar1,
.bar2,
.bar3 {
	width: 35px;
	height: 5px;
	background-color: #fff;
	margin: 6px 0;
	transition: 0.4s;
}
.nav-ul {
	display: none;
}
.header {
	height: 120px;
}
img {
	margin-left: 130px;
}
.navbar {
	width: 50%;
}
.navbar:nth-child(3) {
	margin-right: 10px;
}

a {
	margin-left: 30px;
	margin-right: 30px;
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
	top: 20px;
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
	width: 120%;
}
.submit-application::after {
	content: "";
	width: 120%;
	position: absolute;
	left: 0;
	bottom: -4px;
	border-width: 0 0 2px;
	border-style: solid;
}
.submit-application:after:hover::before {
	transform: scaleX(1);
}

@media only screen and (max-width: $bp-tablet) {
	.navbar {
		display: none;
	}
	.button {
		display: block;
		margin-right: 20px;
	}
	.nav-ul {
		display: inline-block;
		position: fixed;
		left: 0;
		margin: 0;
		padding: 0;
		background-color: $heading-text;
		top: -200px;
		list-style-type: none;
		li {
			height: 50px;
			text-align: center;
			width: 100vw;
		}
	}
	img {
		margin-left: 10px;
	}
}
</style>
