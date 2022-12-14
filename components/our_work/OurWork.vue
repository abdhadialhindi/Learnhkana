<template>
  <div class="mt-15 ps-18">
    <v-container>
      <v-row
       justify="center"
      >
        <v-col  cols="12" >
          <v-row
            justify="center"
          >
            <article
              class="pa-2 primary-color article"
              :class="$vuetify.breakpoint.name == 'sm' ? 'article-md' : ''"
            >
              <h2 class="text-center">Check our awesome</h2>
              <h2 class="divider text-center">creative work</h2>
              <!-- <v-divider
                width="130"
                length="5"
                :class="$vuetify.rtl ? 'thick-one' : 'thick-tow'"
                class="thick"
              ></v-divider> -->
              <p class="text-center">
               Get learning solution that's tailored to your needs
              </p>
            </article>
          </v-row>
        </v-col>

      </v-row>
    </v-container>
    <v-container>
    <v-row justify="center" class="mt-3">
      <v-col sm="12" lg="12" md="12" cols="12">
        <v-row justify="center">
          <!-- <div class="slide-group-width"> -->
            <v-slide-group class="pa-1 ma-4" >
              <template v-slot:next>
                <v-icon
                  color="primary"
                  large
                  :class="$vuetify.rtl ? 'icon-one' : 'icon-tow'"
                  >{{ `mdi-arrow-${$vuetify.rtl ? "left" : "right"}` }}</v-icon
                >
              </template>
              <template v-slot:prev>
                <v-icon
                  color="primary"
                  large
                  :class="$vuetify.rtl ? 'icon-tow' : 'icon-one'"
                  >{{ `mdi-arrow-${$vuetify.rtl ? "right" : "left"}` }}</v-icon
                >
              </template>
              <v-slide-item v-for="(item, index) in items" :key="index">
                <v-card color="#fff " class="me-4 card-width" width="370" relative>
                  <v-container class="mt-2">
                    <v-row justify="center">
                      <img
                        src="@/assets/images/ourwork/39a1bf8b-7e3f-48e4-af71-5912d4ad7704.jpeg"
                        class="white--text align-end img-border"
                        height="220px"
                      />
                    </v-row>
                  </v-container>

                  <v-card-title class="color-primary">
                    {{ item.title }}
                  </v-card-title>
                  <v-card-subtitle class="pb-0 me-5 pe-2">
                    {{ item.desc }}
                  </v-card-subtitle>

                  <v-card-actions>
                    <v-spacer></v-spacer>

                    <v-btn
                      icon

                      bottom
                      right
                      class="border-primary"
                      :class="$vuetify.rtl ? 'end-0' : ''"
                    >
                      <v-icon color="primary" large class="color">{{
                        `mdi-arrow-${$vuetify.rtl ? "left" : "right"}`
                      }}</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-slide-item>
            </v-slide-group>
          <!-- </div> -->
        </v-row>
      </v-col>
    </v-row>
    <v-row justify="center" class="mt-5 mb-3">
      <v-btn
              color="primary"
              rounded
              height="50"
              width="170"


              class="mt-2 mb-2 end-media"
              ><span class="white--text">View all work</span></v-btn
            >
    </v-row>
  </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: "Pre-fab homes",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Etdignissimos, architecto, quam modi ipsum animi nostrum eveniet.",
        },
        {
          title: "Favorite road trips",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Etdignissimos, architecto, quam modi ipsum animi nostrum eveniet.",
        },
        {
          title: "Best airlines",
          desc:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Etdignissimos, architecto, quam modi ipsum animi nostrum eveniet.",
        },
        {
          title:"learnkhana",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Etdignissimos, architecto, quam modi ipsum animi nostrum eveniet.",

        },
      ],
      disabled: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  h2,
  p {
    color: var(--color-primary);
  }
}
.article-md {
  text-align: center;
  h2 {
    font-size: 32px;
  }
  // .thick-one {
  //   transform: translateX(-150%);
  // }
  // .thick-tow {
  //   transform: translateX(150%);
  // }

}
.divider::before {
    content: "";
    width: 130px;
    height: 3px;
    background-color: var(--color-secondary);
    position: absolute;
    bottom: 0px;

    left: 50%;
    -moz-transform: translateX(-50%);
    -webkit-transform: translateX(-50%);
  }
.slide-group-width {
  // width: 1030px;
}
.img-border {
  border-radius: 10px;
}
.thick {
  border-width: 2px;
  background: var(--color-secondary) !important;
}
.end-0 {
  // right: 88%;
}
.icon-one {
  border: 2px solid var(--color-primary);
  border-radius: 50%;
  width: 50px;
  height: 50px;
  pointer-events: auto !important;
}
.left {
  left: 0;
  position: absolute;
}
.icon-tow {
  border: 2px solid var(--color-primary);
  border-radius: 50%;
  width: 50px;
  height: 50px;
  pointer-events: auto !important;
}
.color-primary {
  color: var(--color-primary);
}
.icon-one:hover {
  position: absolute;
  transform: translatex(-50%);
  z-index: 2;
  transition: 0.5s;
  opacity: 1;
  background-color: var(--color-primary);
  color: #fff !important;
}
.icon-tow:hover {
  position: absolute;
  transform: translatex(50%);
  z-index: 2;
  transition: 0.5s;
  opacity: 1;
  background-color: var(--color-primary);
  color: #fff !important;
}
.divider {
  position: relative;
}

.border-primary {
  border: 1px solid var(--color-primary);
}
.border-primary:hover{
  background-color: var(--color-primary);
}
.color:hover{
  color: #fff !important;
}
@media (width<767px) {
  .icon-one {
    display: none;
  }
  .icon-tow {
    display: none;
  }
  .slide-group-width {
    width: 100%;
    // display: flex;
    // justify-content: center;
  }
  .card-width {
    width: 325px !important;
  }
  .end-media {
    margin-top: 15px;
    top: 0;
  }
  .article {
    text-align: center;
    // margin-right: 50px !important;
    padding-left: 0 !important;
    h2 {
      font-size: 24px;
    }
    p {
      margin-top: 32px;
    }
    .thick {
      display: none;
    }
  }
  .divider::before {
    content: "";
    width: 130px;
    height: 3px;
    background-color: var(--color-secondary);
    position: absolute;
    bottom: 0px;
    left: 50%;
    -moz-transform: translateX(-50%);
    -webkit-transform: translateX(-50%);
  }
}
@media (width<1000px) {
  .thick {
    display: none;
  }
  .end-media {
    top: 0;
  }
}
@media (width<325px) {
  .card-width{
    width: 320px !important;
    // margin-left: 0px !important;
    // margin-right: 10 px !important;
  }

}
</style>
