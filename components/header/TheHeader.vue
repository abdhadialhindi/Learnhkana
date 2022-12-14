<template>
  <div>
    <v-navigation-drawer
      class="hidden-md-and-up header-one-page-nav-drawer"
      v-model="drawer"
      fixed
      :right="$vuetify.rtl"
      width="320"
    >
      <v-list-item class="pa-5">
        <div class="logo">
          <img
            style="max-width: 180px !important"
            src="../../assets/images/logo/logo-light.png"
            alt="brand-image"
          />
        </div>
        <v-spacer></v-spacer>
        <v-btn
          class="close-icon"
          icon
          @click="drawer = !drawer"
          v-html="iconSvg(closeIcon)"
        >
        </v-btn>
      </v-list-item>
      <scrollactive
        active-class="v-btn--active"
        bezier-easing-value=".5,0,.35,1"
        :offset="71"
      >
        <v-list>
          <v-list-item
            :ripple="false"
            v-for="item in items"
            :key="item.title"
            :to="localePath(item.to)"
            link
          >
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link :to="'/buy'" class="scrollactive-item">
            <v-list-item-content>
              <v-list-item-title>{{ $t("Contact Us") }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </scrollactive>
    </v-navigation-drawer>

    <v-app-bar
      color="transparent"
      fixed
      elevate-on-scroll
      class="header-one-page-nav"
    >
      <router-link to="/" class="logo">
        <slot name="logo"></slot>
        <slot name="logo-dark"></slot>
      </router-link>
      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-xs-only hidden-sm-only height-auto">
        <scrollactive
          active-class="v-btn--active"
          bezier-easing-value=".5,0,.35,1"
          :offset="71"
        >
          <v-btn
            :id="item.title"
            v-for="item in items"
            @click="deleteActiveHome"
            :key="item.title"
            :to="localePath(item.to)"
            :ripple="false"
            text
            link
            >{{ item.title }}</v-btn
          >
        </scrollactive>
      </v-toolbar-items>
      <a
        v-if="$vuetify.breakpoint.name == 'lg'"
        class="btn-default btn-border btn-opacity ms-10 me-10"
        target="_blank"
        href="https://themeforest.net/checkout/from_item/32012548?license=regular"
      >
        <span>{{ $t("Contact Us") }}</span>
      </a>
      <v-btn text color="primary" @click="changeLang">
        <v-icon left> mdi-web </v-icon>
        {{ $t("LANG") }}
      </v-btn>
      <v-btn
        icon
        :ripple="false"
        class="ma-0 pa-0 hidden-md-and-up menu_icon"
        @click="drawer = !drawer"
        v-html="iconSvg(icon)"
      >
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
import feather from "feather-icons";
export default {
  data() {
    return {
      drawer: false,
      icon: "menu",
      closeIcon: "x",
    };
  },
  computed: {
    items() {
      return [
        {
          title: this.$t("Home"),
          to: "/",
        },
        {
          title: this.$t("Services"),
          to: "/services",
        },
        {
          title: this.$t("About Us"),
          to: "/about-us",
        },
        {
          title: this.$t("Why Us"),
          to: "/why-us",
        },
        {
          title: this.$t("Blog"),
          to: "/blog",
        },
      ];
    },
  },
  mounted() {
    this.deleteActiveHome();
  },
  methods: {
    deleteActiveHome() {
      var element = document.getElementById("الرئيسية");
      setTimeout(() => {
        if (element) {
          if (
            this.$i18n.locale == "ar" &&
            this.$route.path !== "/" &&
            this.$route.path !== "/ar"
          ) {
            element.classList.remove("v-btn--active");
          } else {
            element.classList.add("v-btn--active");
          }
        }
      }, 100);
    },
    changeLang() {
      this.$router.push(
        this.switchLocalePath(this.$i18n.locale == "ar" ? "en" : "ar")
      );
      this.$vuetify.rtl = !this.$vuetify.rtl;

      this.deleteActiveHome();
    },
    iconSvg(icon) {
      return feather.icons[icon].toSvg();
    },
  },
};
</script>
