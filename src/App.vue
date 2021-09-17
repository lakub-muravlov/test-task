<template>
<Intro>
  <Header/>
</Intro>
</template>

<script>

import Intro from "@/components/Intro";
import Header from "@/components/Header"
export default {
  name: 'App',
  components: {
    Intro,
    Header
  }
}
</script>

<style lang="scss">
@import "src/assets/styles/styles";
</style>
