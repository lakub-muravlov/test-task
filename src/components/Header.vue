<template>
	<header class="header flex fd-row jc-sb ai-center content-container">
		<div class="col-5">
			<img src="../assets/styles/img/logo-header.svg" alt="" />
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
};
</script>

<style scoped lang="scss">
@import "/src/assets/styles/variables.scss";
.header {
	height: 120px;
}
img {
	margin-left: 100px;
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
a:hover {
	color: $intro-text;
}
a::before {
	content: "";
	position: absolute;
	display: block;
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
.submit-application {
}
</style>
