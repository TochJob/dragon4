<template>
  <div id="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Footer from "@/components/layout/Footer.vue";
import Header from "@/components/layout/Header.vue";
export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
};
</script>

<style lang="scss"> 
@import "@/assets/css/fonts.scss";
* {
  margin: 0%;
  padding: 0%;
  box-sizing: border-box;
  font-family: "Raleway";
}
#app {
  background: #151b3d;
  min-height: 100vh;
}
.button {
  cursor: pointer;
  text-decoration: none;
  
}
a{
  transition: all .3s;
  &:hover{
    opacity: .8; 
  }
}
.column{
  display: flex;
  flex-direction: column;
}
.wrapper {
  display: flex;
}

section,
footer {
  padding: 0 calc(50% - 650px);
}
@media (min-width: 319.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 140px);
  }
}

@media (min-width: 479.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 225px);
  }
}

@media (min-width: 575.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 270px);
  }
}

@media (min-width: 767.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 360px);
  }
}

@media (min-width: 991.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 480px);
  }
}

@media (min-width: 1199.98px) {
  section,
  footer {
    padding: 0 calc(50vw - 590px);
  }
}
</style>
