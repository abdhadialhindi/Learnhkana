<template>
  <div class="rn-team-area pb--120 pt--20 bg_color--5">
    <vue-particles
      color="#2852a0"
      :particleOpacity="0.7"
      :particlesNumber="40"
      shapeType="circle"
      :particleSize="4"
      linesColor="#fab120"
      :linesWidth="1"
      :lineLinked="true"
      :lineOpacity="0.4"
      :linesDistance="180"
      :moveSpeed="6"
      :hoverEffect="true"
      hoverMode="repulse"
      :clickEffect="false"
      clickMode="push"
    >
    </vue-particles>
    <v-container>
      <v-row>
        <v-col cols="12">
          <div class="section-title text-center mb--20 mb_sm--0">
            <title-section
              :stick="true"
              :sub-title="subtitle"
              :desc="desc"
            ></title-section>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          lg="3"
          md="3"
          sm="6"
          cols="12"
          class="single_im_portfolio pb--20"
          v-for="(item, i) in portfolioContent"
          :key="i"
        >
          <div class="im_portfolio">
            <div class="thumbnail_inner">
              <div class="thumbnail">
                <a href="portfolio-details.html">
                  <img class="w-100" :src="item.src" alt="Portfolio Images" />
                </a>
              </div>
            </div>
            <div class="content">
              <div class="inner">
                <div class="portfolio_heading">
                  <div class="category_list">
                    <router-link to="/portfolio-details">{{
                      item.category
                    }}</router-link>
                  </div>
                  <h4 class="heading-title">
                    <router-link to="/portfolio-details">{{
                      item.title
                    }}</router-link>
                  </h4>
                </div>
                <div class="portfolio_hover">
                  <router-link to="/blog-details" class="rn-btn btn-opacity">
                    Read More
                  </router-link>
                </div>
              </div>
            </div>
            <router-link
              class="transparent_link"
              to="/portfolio-details"
            ></router-link>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subtitle: "our services",
      desc: "What we promise to the highest quality services",
      portfolioContent: [
        {
          src: require("../../assets/images/portfolio/portfolio-8.jpg"),
          category: "Development",
          title: "Web Design",
          description:
            "Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.",
        },
        {
          src: require("../../assets/images/portfolio/portfolio-9.jpg"),
          category: "Product Design",
          title: "App Development",
          description:
            "Lorem ipsum dolor sit amet, consec tetur adipiscing elit.",
        },
        {
          src: require("../../assets/images/portfolio/portfolio-4.jpg"),
          category: "Design",
          title: "Photoshop",
          description:
            "Lorem ipsum dolor sit amet, consec tetur adipiscing elit.",
        },
        {
          src: require("../../assets/images/portfolio/portfolio-5.jpg"),
          category: "Shop",
          title: "Woocommerce",
          description:
            "Lorem ipsum dolor sit amet, consec tetur adipiscing elit.",
        },
      ],
    };
  },
};
</script>
