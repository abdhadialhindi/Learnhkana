<template>
  <div id="home">
    <CoolLightBox :items="[sliderContent]" :index="index" @close="index = null">
    </CoolLightBox>
    <div class="im_modern_slider overlay_slider" id="home">
      <div class="slide slider-paralax d-flex bg_image bg_gif">
        <v-container>
          <v-row :class="{ 'ps-16': $vuetify.breakpoint.name == 'lg' }">
            <v-col cols="12">
              <div class="inner" :class="'text-start'">
                <h1 class="heading-title">{{ sliderContent.title }}</h1>
                <p class="description">
                  {{ sliderContent.desc }}
                </p>
                <div class="slide-btn">
                  <router-link class="btn-default" to="/contact">{{
                    $t("Get started")
                  }}</router-link>
                  <v-btn
                    color="secondary"
                    class="ma-2 white--text"
                    fab
                    dense
                    @click="index = i"
                  >
                    <v-icon dark> mdi-play </v-icon>
                  </v-btn>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";

export default {
  components: { VueSlickCarousel },
  data() {
    return {
      index: null,
      sliderContent: {
        className: "text-start",
        img: "https://media.giphy.com/media/ZqlvCTNHpqrio/giphy.gif",
        title: this.$t("Learning is What Drives The Next Era of Business."),
        desc: this.$t("We're the all-in-one learning solution that provides impactful programmes for everyone."),
        src: "https://www.youtube.com/watch?v=ZOoVOfieAF8",
      },
      settings: {
        fade: true,
        dots: true,
        arrows: true,
        infinite: true,
        speed: 1000,
        slidesToShow: 1,
        slidesToScroll: 1,
        margin: 20,
        adaptiveHeight: true,
      },
    };
  },
};
</script>

<style lang="scss">
.overlay_slider {
  position: relative;
}
.overlay_slider::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(255, 255, 255, 0.4) !important;
}
.slick-slide {
  img {
    display: block;
    width: 100%;
  }
}
.bg_gif {
  background-image: url("https://media.giphy.com/media/ZqlvCTNHpqrio/giphy.gif");
}
</style>
