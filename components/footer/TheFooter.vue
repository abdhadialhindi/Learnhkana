<template>
  <footer class="footer-area footer-style-01 bg_color">
    <v-row justify="center">
      <v-col cols="10">
        <!-- <div class="im-call-to-action-area ptb--70 im-separator">
      <v-container>
        <v-row class="align-center">
          <v-col xl="6" lg="8" md="6" sm="12" cols="12">
            <div class="inner">
              <h2 class="white--text mb--0">
                Enough Talk, Let's Build Something Together
              </h2>
            </div>
          </v-col>
          <v-col lg="4" offset-xl="2" md="6" sm="12" cols="12">
            <div
              class="text-start call-to-cation-tbn text-md-right mt_md--20 mt_sm--20"
            >
              <router-link
                class="btn-default btn-large btn-border btn-opacity"
                to="/contact"
                >Read Out Now</router-link
              >
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div> -->
        <div class="footer-wrapper ptb--70">
          <v-container class="container">
            <v-row justify="center">
              <v-col lg="4" md="4" sm="6" cols="12">
                <div class="ft-text">
                  <div class="logo">
                    <a href="/"><img :src="logo" alt="brand image" /></a>
                  </div>
                  <!-- <p>
                Copyright © {{ new Date().getFullYear() }}
                <a href="/">Imroz</a> VueJs Template. Built with love in
                Bangladesh All rights reserved.
              </p> -->
                  <span
                    >Lorem ipsum dolor sit consectetur, adip elit. Voluptas atque officia
                    aspernatur saepe.</span
                  >
                </div>
              </v-col>
              <v-col lg="2" offset-xl="1" md="6" sm="6" cols="12" class="mt_mobile--40">
                <div class="footer-link">
                  <h4>Quick Link</h4>
                  <ul class="ft-link">
                    <li><router-link to="/portfolio">Service</router-link></li>
                    <!-- <li><router-link to="/about">About</router-link></li> -->
                    <li><router-link to="/blog">Blog</router-link></li>
                    <!-- <li><router-link to="/team">Our Team</router-link></li> -->
                    <!-- <li><router-link to="/contact">Contact</router-link></li> -->
                  </ul>
                </div>
              </v-col>
              <v-col lg="2" md="2" sm="6" cols="12" class="mt_md--40 mt_sm--40">
                <div class="footer-link">
                  <h4>contact us</h4>
                  <ul class="ft-link">
                    <li><router-link to="/service">Location</router-link></li>
                    <li><router-link to="/gallery">Number</router-link></li>
                    <li><router-link to="/pricing-plan">REQ Services</router-link></li>
                    <li>
                      <router-link to="/video-popup">Landing Page</router-link>
                    </li>
                    <!-- <li>
                  <router-link to="/office-location"
                    >Office Location</router-link
                  >
                </li> -->
                  </ul>
                </div>
              </v-col>
              <v-col lg="4" md="4" sm="6" cols="12">
              <div class="footer-link">
                <h4>Join our newsletter.</h4>
                <v-text-field
                class="color"
                  is-booted
                  placeholder="Enter your e-mail"
                  solo
                  rounded
                  elevation-12
                  enclosed

                ><template v-slot:append >
                  <v-icon
                    color="primary"
                    :class="$vuetify.rtl ? 'move-icon': ''"

                    >mdi-send</v-icon
                  >
                </template></v-text-field>
                <span>Waiting for your message is not your important time</span>
              </div>
              </v-col>
            </v-row>
            <v-divider class="mt-16" color="#fff"></v-divider>
            <v-row justify="space-between">
            <v-col md="4" sm="12" xs="12" cols="12">
            <span class="color-p">
              Copyright © {{ new Date().getFullYear() }}.All Rights Reserved
            </span>
          </v-col>

            <v-col md="5" sm="12" xs="12">
            <div class="d-flex justify-end align-baseline">
            <p class="me-4  color-p">
            follow us on
            </p>
            <ul class="justify-center social-share d-flex liststyle">
              <li v-for="(social, i) in socialList" :key="i" >
                <a :href="social.url" target="_blank" class="media-icon"
                  ><i class="fab" :class="social.icon"></i
                ></a>
              </li>
            </ul>
          </div>
        </v-col>
            </v-row>
          </v-container>
        </div>
      </v-col>
    </v-row>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      logo: require("../../assets/images/logo/logo-light.png"),
      socialList: [
        {
          icon: "fa-facebook-f",
          url: "https://www.facebook.com/",
        },
        {
          icon: "fa-linkedin-in",
          url: "https://www.linkedin.com/",
        },
        {
          icon: "fa-twitter",
          url: "https://twitter.com/",
        },
        {
          icon: "fa-instagram",
          url: "https://www.instagram.com/",
        },
      ],
    };
  },
};
</script>
<style scoped>
.bg_color {
  background-color: var(--color-primary);
}
.color-p{
  color: #fff !important;
}

.move-icon{
  /* position: absolute; */
  transform: scaleX(-1);
}
@media (width<767px) {
  .media-icon{
    width: 15%;
    border: none;
    margin-left: 8px;
  }


}

</style>
