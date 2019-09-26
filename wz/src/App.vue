<template>
  <div id="app">
    <Ost></Ost>
    <Bg></Bg>
    <Wrapper></Wrapper>
    <Foot></Foot>
  </div>
</template>

<script>
  import Ost from "./components/Ost";
  import Bg from "./components/Bg";
  import Wrapper from "./components/Wrapper";
  import Foot from "./components/Foot";
export default {
  name: 'App',
    components:{
        Ost,
        Bg,
        Wrapper,
        Foot

    }
}
</script>

<style lang="scss">
@import "style1.scss";
</style>
