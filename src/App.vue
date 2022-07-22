<template>
  <div id="app">
    <Banner />
    <Introduce />
    <Brand />
    <Compared />
    <Serve />
    <Advertising />
    <Operation />
    <Case />
    <Footer />
  </div>
</template>

<script>
import Serve from "./components/Serve.vue";
import Banner from "./components/Banner.vue";
import Compared from "./components/Compared.vue";
import Introduce from "./components/Introduce.vue";
import Brand from "./components/Brand.vue";
import Advertising from "./components/Advertising.vue";
import Operation from "./components/Operation.vue";
import Case from "./components/Case.vue";
import Footer from "./components/Footers.vue";

export default {
  components: { Serve, Banner, Compared, Introduce, Brand,Advertising,Operation,Case, Footer },
};
</script>

<style lang="less">
::-webkit-scrollbar {
  width: 4px;
  height: 4px;
}

::-webkit-scrollbar-thumb {
  border-radius: 8px;
  background: rgba(0, 0, 0, 0.2);
  box-shadow: inset 0 0 5px rgb(0 0 0 / 20%);
}

::-webkit-scrollbar-track {
  border-radius: 0;
  background: rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 0 5px rgb(0 0 0 / 20%);
}

@keyframes bottomShow {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }

  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}

html,
body {
  height: 100%;
  background: #FFFFFF;
}

#app {
  height: 100%;
  background: #FFFFFF;
}

.row {
  --bs-gutter-x: 24px !important;
  // margin: 0 !important;
}

.adapterMixin();
@media (min-width:1400px) {
  .container{
    max-width: 1344px !important;
    padding: 0 !important;
  }
}
</style>
