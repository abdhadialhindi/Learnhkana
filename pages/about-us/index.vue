<template>
  <div class="relative">
    <div
      class="breadcrumb-area rn-bg-color ptb--120 bg_image bg_image--1"
      data-black-overlay="6"
    >
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="breadcrumb-inner pt--100 pt_sm--40 pt_md--50">
              <h2 class="heading-title">{{ $t("About us") }}</h2>
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

    <div>
      <v-container>
        <h2 class="text-center mt-5 mb-5">Who we are</h2>
        <p class="text-center">
          We are a Regional Edtech company Providing integrated ecosystems of ready-made,
          customized learning solutions in One Place! To corporates, providers,
          government, NGOs, and individuals. Through our platforms, learning design, and
          consulting services Empowered by innovation technology and team learning
          expertise. Our purpose is to Build impactful, engaging, and fit-of-purpose
          learning experiences.
        </p>
      </v-container>
    </div>
    <v-row justify="center" class="pr-4 pl-4">
      <div class="timeline mt-10">
        <v-timeline class="">
          <v-timeline-item class="text-center" height="200">
            <p class="text-center">2018</p>
            Learnkhana starts as a learning designing firm under the name of “Learning
            Lap”
          </v-timeline-item>
          <v-timeline-item class="text-center"
            ><p class="text-center">2019</p>
            Launching of our Learnkhana platform with a mission of “Better career and
            personal lives for youth”
          </v-timeline-item>
          <v-timeline-item
            ><p class="text-center">2020</p>
            Learnkhana was incubated by the Egyptian Ministry of telecommunications and
            information Technology as a promising company.
          </v-timeline-item>
          <v-timeline-item
            ><p class="text-center">2021</p>
            We established our compliance arm, to expand our offering in the Mena region,
            and especially Gulf countries.
          </v-timeline-item>
          <v-timeline-item
            ><p class="text-center">2022</p>
            We are on a mission of “expansion”.
          </v-timeline-item>
        </v-timeline>
      </div>
    </v-row>
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
                    {{ $t("Our Success story.") }}
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
              <h2>{{ $t("Who we are?") }}</h2>
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
          title: this.$t("Our vision."),
          desc: this.$t(
            `To be an instrument of ensuring every organizational success and growth hand in hand, by providing world-class learning solutions that will shape the future of corporate learning technology solutions. `
          ),
        },
        {
          title: this.$t("Our Mission"),
          desc: this.$t(
            `What do we do every day to get where we want to be?
            We take a value-driven approach to every training we undertake to help organizations achieve their business objectives by helping them train their employees, partners, and clients effectively, thus improving the performance of individuals and teams through our learning solutions.`
          ),
        },
        {
          title: this.$t("Our values."),
          desc: this.$t(
            `In a competitive business world, a set of developed values are a crucial mainstay of our company philosophy. We base our relationships on trust and aim to act fairly and ethically at all times.`
          ),
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
        `Learnkhana started its journey in 2018, built around one goal; to become the most preferred strategic partner of corporate learning technology solutions while having an expert staff and the latest technological abilities.

Since our start, we are working passionately to provide the best quality and service for our partners all around the world.


+5
YEARS OF
EXPERIENCE`
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

<style scoped lang="css">
.relative {
  position: relative;
  margin-top: 128px;
  margin-bottom: 36px;
}
.timeline {
  height: 300px;
  position: relative;
  overflow-y: auto;
  width: 100%;
}
::-webkit-scrollbar {
  width: 4px;
  height: 4px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: var(--color-primary);
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: var(--color-secondary);
}
@media (width<767px) {
  .timeline {
    width: 100%;
  }
}
</style>
