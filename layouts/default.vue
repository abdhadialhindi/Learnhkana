<template>
  <v-app dark>
    <v-overlay :value="loader" color="white" opacity="1" z-index="100">
      <img :src="logoLight" width="100%" />
    </v-overlay>
    <template v-if="!loader">
      <the-header>
        <img slot="logo" :src="logoLight" class="logo-light" />
        <img slot="logo-dark" :src="logoDark" class="logo-dark" />
      </the-header>
      <v-main>
        <Nuxt />
      </v-main>
      <the-footer></the-footer>
    </template>
    <v-fab-transition>
      <v-btn
        v-scroll="onScroll"
        v-show="fab"
        fab
        color="primary"
        fixed
        width="50"
        height="50"
        bottom
        right
        @click="toTop"
        class="scroll-fab"
      >
        <svg
          stroke="currentColor"
          fill="none"
          stroke-width="2"
          viewBox="0 0 24 24"
          stroke-linecap="round"
          stroke-linejoin="round"
          height="1em"
          width="1em"
          xmlns="http://www.w3.org/2000/svg"
        >
          <polyline points="18 15 12 9 6 15"></polyline>
        </svg>
      </v-btn>
    </v-fab-transition>
  </v-app>
</template>

<script>
import TheFooter from "../components/footer/TheFooter";
import TheHeader from "../components/header/TheHeader";

export default {
  components: { TheFooter, TheHeader },
  name: "DefaultLayout",
  data() {
    return {
      fab: false,
      loader: true,
      logoLight: require("../assets/images/logo/logo-light.png"),
      logoDark: require("../assets/images/logo/logo-dark.png"),
    };
  },
  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    },
  },
  mounted() {
    if (this.$i18n.locale == "ar") {
      this.$vuetify.rtl = true;
    }
    if (process.browser) {
      const self = this;
      window.onNuxtReady(() => {
        self.loader = false;
      });
    }
  },
};
</script>
<style scoped lang="scss">
.v-btn--fab.v-btn--contained {
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);
}
.v-btn--icon.v-size--default .v-icon,
.v-btn--fab.v-size--default .v-icon {
  height: 30px;
  font-size: 30px;
  width: 30px;
}
.v-btn--fab.v-btn--fixed {
  z-index: 99;
}
.v-btn--absolute.v-btn--bottom,
.v-btn--fixed.v-btn--bottom {
  bottom: 60px;
}

.v-btn--absolute.v-btn--right,
.v-btn--fixed.v-btn--right {
  right: 20px;
}
.scroll-fab {
  &.white {
    border: none;
  }
  svg {
    font-size: 24px;
  }
}
</style>
