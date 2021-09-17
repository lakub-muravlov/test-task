<template>
	<Intro>
		<Header />
		<IntroText />
	</Intro>
	<Footer />
</template>

<script>
import Intro from "@/components/Intro";
import Header from "@/components/Header";
import IntroText from "@/components/IntroText";
import Footer from "@/components/Footer";
export default {
	name: "App",
	components: {
		Intro,
		Header,
		IntroText,
		Footer,
	},
};
</script>

<style lang="scss">
@import "src/assets/styles/styles";
</style>
