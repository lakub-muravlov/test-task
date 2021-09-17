<template>
	<Intro>
		<Header />
		<IntroText />
	</Intro>
	<Advantages />
	<Beliefs />
	<Footer />
</template>

<script>
import Intro from "@/components/Intro";
import Header from "@/components/Header";
import IntroText from "@/components/IntroText";
import Advantages from "@/components/Advantages";
import Beliefs from "@/components/Beliefs";
import Footer from "@/components/Footer";
export default {
	name: "App",
	components: {
		Intro,
		Header,
		IntroText,
		Advantages,
		Beliefs,
		Footer,
	},
};
</script>

<style lang="scss">
@import "src/assets/styles/styles";
</style>
