<template>
  <div class="pt--120">
    <v-container>
      <v-row justify="center">
        <v-col cols="10" md="8" xs="12" sm="12">
          <title-section
            class="mt-7 mb-16"
            title="News and insights"
            sub-title=""
            desc="it is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout"
          ></title-section>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="4" xs="12">
          <v-card color="#fff " class="ma-4 border" relative elevation="24">
            <v-container class="mt-2">
              <v-row justify="center">
                <img
                  src="@/assets/images/ourwork/39a1bf8b-7e3f-48e4-af71-5912d4ad7704.jpeg"
                  class="white--text align-end border"
                  contain
                />
              </v-row>
            </v-container>

            <v-card-subtitle class="pb-0 me-5 pe-2"
              ><v-icon color="primary" class="me-2">mdi-calendar-month</v-icon
              ><span>22 nov 2018</span>
              <v-icon color="primary" class="ms-2 me-2">mdi-comment</v-icon>
              <span>2 comments</span>
            </v-card-subtitle>

            <v-card-title class="mb-16" style="height: 120px"
              >At Vero eos et accusamus et odio dignissimos
            </v-card-title>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn text color="primary" class="button">
                Read more
                <v-icon small>{{(`mdi-chevron-${$vuetify.rtl ? "left" : "right"}-circle`)}}</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12" md="4" xs="12">
          <v-card color="#fff " class="ma-4 border" relative elevation="24">
            <v-container class="mt-2">
              <v-row justify="center">
                <img
                  src="@/assets/images/ourwork/39a1bf8b-7e3f-48e4-af71-5912d4ad7704.jpeg"
                  class="white--text align-end border"
                  contain
                />
              </v-row>
            </v-container>

            <v-card-subtitle class="pb-0 me-5 pe-2"
              ><v-icon color="primary" class="me-2">mdi-calendar-month</v-icon
              ><span>22 nov 2018</span>
              <v-icon color="primary" class="ms-2 me-2">mdi-comment</v-icon>
              <span>2 comments</span>
            </v-card-subtitle>

            <v-card-title class="mb-16" style="height: 120px"
              >At Vero eos et accusamus et odio dignissimos
            </v-card-title>

            <v-card-actions>
              <v-spacer></v-spacer>

              <v-btn text color="primary" class="button">
                Read more
                <v-icon small>{{(`mdi-chevron-${$vuetify.rtl ? "left" : "right"}-circle`)}}</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="12" md="4" xs="12">
          <h2 class="text-color mt-7">Get The Latest News Here</h2>
          <v-row justify="center" class="mb-5">
            <v-col cols="6">
              <img
                src="@/assets/images/ourwork/39a1bf8b-7e3f-48e4-af71-5912d4ad7704.jpeg"
                class="white--text align-end border"
                style="width: 100%"
              />
            </v-col>
            <v-col cols="6">
              <article>
                <span class="">09 April 2021</span>
                <span>by Admin</span>
                <p class="paraghraph">
                  lorem ipsum dolor sit amit, consecte adipiscing elit est ullamcorper
                </p>
              </article>
            </v-col>
          </v-row>
          <v-row justify="center">
            <v-col cols="6">
              <img
                src="@/assets/images/ourwork/39a1bf8b-7e3f-48e4-af71-5912d4ad7704.jpeg"
                class="white--text align-end border"

              />
            </v-col>
            <v-col cols="6">
              <article>
                <span class="">09 April 2021</span>
                <span>by Admin</span>
                <p class="paraghraph">
                  lorem ipsum dolor sit amit, consecte adipiscing elit est ullamcorper
                </p>
              </article>
            </v-col>
          </v-row>
          <v-row :justify="`${$vuetify.breakpoint.name == 'xs' ? 'center' : 'start'}`">
            <v-btn rounded color="primary" class="mt-3 margin">Read more</v-btn>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style>
.border {
  border-radius: 10px !important;
}
.text-color {
  color: var(--color-primary);
  font-size: 40px;
}
.paraghraph {
  font-size: 12px !important;
  display: block;
}
.button {
  border: 0px !important;
}
@media (width<767px) {
  .text-color {
    text-align: center;
    font-size: 24px;
  }
  .margin {
    margin-bottom: 20px;
  }
}
</style>
