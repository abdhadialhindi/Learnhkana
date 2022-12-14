<template>
  <div>
    <div
      class="breadcrumb-area rn-bg-color ptb--120 bg_image bg_image--1"
      data-black-overlay="6"
    >
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="breadcrumb-inner pt--100 pt_sm--40 pt_md--50">
              <h2 class="heading-title">{{ $t("Why Us") }}</h2>
              <ul class="page-list">
                <li v-for="(item, i) in breadcrumbs" :key="i">
                  <router-link :to="item.to" :disabled="item.disabled">{{
                    item.text
                  }}</router-link>
                </li>
              </ul>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="about-area ptb--120 bg_color--1">
      <div class="about-wrapper">
        <v-container>
          <v-row align="center" class="row--35">
            <v-col lg="5" md="5" cols="12">
              <div class="thumbnail">
                <img
                  slot="thum-img"
                  class="w-100"
                  src="@/assets/images/about/about-1.png"
                  alt="About Images"
                />
              </div>
            </v-col>
            <v-col lg="7" md="7" cols="12">
              <div class="about-inner inner">
                <div class="section-title">
                  <div class="icon" v-html="iconSvg(icon)"></div>
                  <h2 class="heading-title">
                    {{ $t("Why Learnkhana") }}
                  </h2>
                  <p class="description">{{ desc }}</p>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </div>
    <div class="service-area ptb--120 bg_color--5">
      <v-container>
        <v-row>
          <v-col cols="12">
            <div class="text-center section-title mb--30">
              <h2>{{ $t("What Makes Our Work Unique?") }}</h2>
              <!-- <p>
                There are many variations of passages of Lorem Ipsum available,
                <br />
                but the majority have suffered alteration.
              </p> -->
            </div>
          </v-col>
        </v-row>
        <!-- End .row -->
        <div class="service-white-wrapper">
          <v-row class="service-main-wrapper mt_dec--30">
            <!-- Start Single Service  -->
            <v-col
              lg="4"
              md="4"
              sm="6"
              cols="12"
              v-for="(service, i) in serviceContent"
              :key="i"
            >
              <div class="service service__style--2 text-start bg-gray">
                <router-link to="/service-details">
                  <div class="service">
                    <!-- <div class="icon" v-html="iconSvg(service.icon)"></div> -->
                    <div class="content">
                      <h3 class="heading-title">{{ service.title }}</h3>
                      <p>
                        {{ service.desc }}
                      </p>
                    </div>
                  </div>
                </router-link>
              </div>
            </v-col>
            <!-- End Single Service  -->
          </v-row>
        </div>
      </v-container>
    </div>
  </div>
</template>

<script>
import feather from "feather-icons";

export default {
  data() {
    return {
      icon: "send",
    };
  },
  computed: {
    serviceContent() {
      return [
        {
          title: this.$t("One-stop Shop."),
          desc: this.$t(`We provide you customizable learning journeys, at speed and price that will delight you, not only that but also journeys that suit your company’s needs.`),
        },
        {
          title: this.$t("Expert LXD Team."),
          desc: this.$t(`Our team’s years of experience make us a dynamic technology partner, who can harness modern technology to accelerate and utilize.`),
        },
        {
          title: this.$t("Utilizing Media Tools"),
          desc: this.$t(`Development to reduce timelines.We determine the appropriate technology solutions and project methodologies that meet your company’s goals.`),
        },
      ];
    },
    breadcrumbs() {
      return [
        {
          text: this.$t("Home"),
          to: "/",
          disabled: false,
        },
        {
          text: this.$t("Why Us"),
          to: "",
          disabled: true,
        },
      ];
    },
    desc() {
      return this.$t(
        `LearnKhana is a regional Edtech Company Providing an Integrated ecosystem of ready-made and customized learning solutions at one place. We build impactful, Engaging, and Fit for purpose learning experiences.For over 5 years, LearnKhana has successfully delivered learning solutions to 100+ clients.`
      );
    },
  },
  methods: {
    iconSvg(icon) {
      return feather.icons[icon].toSvg();
    },
  },
};
</script>

<style></style>
