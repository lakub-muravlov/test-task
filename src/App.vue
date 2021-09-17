<template>
	<Intro>
		<Header />
		<IntroText />
	</Intro>
	<Advantages />
	<!--Footer /-->
</template>

<script>
import Intro from "@/components/Intro";
import Header from "@/components/Header";
import IntroText from "@/components/IntroText";
//import Footer from "@/components/Footer";
import Advantages from "@/components/Advantages";
export default {
	name: "App",
	components: {
		Intro,
		Header,
		IntroText,
		//Footer,
		Advantages,
	},
};
</script>

<style lang="scss">
@import "src/assets/styles/styles";
</style>
