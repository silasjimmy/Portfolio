<template>
  <v-app>
    <!-- App bar -->
    <v-app-bar
      app
      dark
      shrink-on-scroll
      flat
      prominent
      src="https://picsum.photos/1920/1080?random"
      scroll-target="#main"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5), rgba(0,0,0,.8)"
        ></v-img>
      </template>

      <v-app-bar-title>Portfolio</v-app-bar-title>

      <v-spacer></v-spacer>

      <!-- Theme switch -->
      <v-switch
        inset
        hide-details
        color="success"
        class="py-3"
        v-model="appTheme"
        :label="appTheme ? 'Dark theme' : 'Light theme'"
      ></v-switch>

      <template v-slot:extension>
        <v-tabs
          fixed-tabs
          center-active
          icons-and-text
          show-arrows
          color="success"
          v-model="tab"
        >
          <v-tabs-slider></v-tabs-slider>
          <v-tab href="#about" class="text-capitalize">
            <span>About</span>
            <v-icon>mdi-account-star</v-icon>
          </v-tab>

          <v-tab href="#education" class="text-capitalize">
            <span>Education</span>
            <v-icon>mdi-school</v-icon>
          </v-tab>

          <v-tab href="#work" class="text-capitalize">
            <span>Work</span>
            <v-icon>mdi-briefcase</v-icon>
          </v-tab>

          <v-tab href="#experience" class="text-capitalize">
            <span>Experience</span>
            <v-icon>mdi-weight-lifter</v-icon>
          </v-tab>
        </v-tabs>
      </template>
    </v-app-bar>

    <!-- Content -->
    <v-sheet max-height="100vh" id="main" class="overflow-auto pa-2">
      <v-main>
        <v-card outlined class="rounded-lg">
          <v-tabs-items v-model="tab">
            <v-tab-item value="about">
              <v-container fluid>
                <v-row>
                  <v-col cols="12" lg="3">
                    <v-card flat>
                      <v-card-text class="pb-0 text-center">
                        <v-avatar size="110px">
                          <v-img src="./assets/img/silas-jimmy.jpg"></v-img>
                        </v-avatar>
                      </v-card-text>

                      <v-card-title class="justify-center text-capitalize"
                        >silas jimmy</v-card-title
                      >

                      <v-card-subtitle class="text-center text-capitalize pb-0"
                        >python programmer || web developer</v-card-subtitle
                      >

                      <v-card-subtitle class="text-center pt-1">
                        <v-chip pill color="transparent">
                          <v-icon left>mdi-map-marker</v-icon>
                          <span class="text-capitalize text--secondary"
                            >mombasa, kenya</span
                          >
                        </v-chip>
                      </v-card-subtitle>

                      <v-card-text class="text-center">
                        Lorem ipsum dolor sit, amet consectetur adipisicing
                        elit. Omnis dolore ipsam blanditiis quam, fuga, labore
                        aliquid ullam sint unde veritatis quibusdam nulla! Sequi
                        ex tempora atque, architecto nemo minus iste!
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col cols="12" lg="9">
                    <v-card flat>
                      <v-card-title class="justify-center"
                        >Hi there,</v-card-title
                      >

                      <v-card-subtitle class="text-center"
                        >I am Silas Jimmy.</v-card-subtitle
                      >

                      <v-card-text class="text-center">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Delectus, aperiam! Magni expedita molestiae doloribus
                        reiciendis id, inventore vitae quia illo eligendi.
                        Reiciendis odit ea quam ab sunt ullam illum tempore!
                      </v-card-text>

                      <v-card-text class="text-center">
                        <v-chip outlined pill class="ma-1">
                          <v-icon left> mdi-email </v-icon>
                          jimmysilas17@gmail.com
                        </v-chip>
                        <v-chip outlined pill class="ma-1">
                          <v-icon left> mdi-phone </v-icon>
                          +254 719 773 594
                        </v-chip>
                      </v-card-text>

                      <v-card-actions class="justify-center">
                        <v-btn icon>
                          <v-icon>mdi-twitter</v-icon>
                        </v-btn>
                        <v-btn icon>
                          <v-icon>mdi-instagram</v-icon>
                        </v-btn>
                        <v-btn icon>
                          <v-icon>mdi-linkedin</v-icon>
                        </v-btn>
                        <v-btn icon>
                          <v-icon>mdi-github</v-icon>
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>

            <v-tab-item value="education">
              <v-card flat>
                <v-card-text>
                  <v-expansion-panels focusable>
                    <v-expansion-panel>
                      <v-expansion-panel-header expand-icon="mdi-menu-down">
                        <v-list-item three-line>
                          <v-list-item-avatar>
                            <v-icon>mdi-certificate</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title class="text-wrap"
                              >BSc Computer Science -
                              Candidate</v-list-item-title
                            >
                            <v-list-item-subtitle
                              >Pwani University, Kilifi
                              Kenya</v-list-item-subtitle
                            >
                            <v-list-item-subtitle
                              >September 2017 - December
                              2021</v-list-item-subtitle
                            >
                          </v-list-item-content>
                        </v-list-item>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat.
                      </v-expansion-panel-content>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-header expand-icon="mdi-menu-down">
                        <v-list-item three-line>
                          <v-list-item-avatar>
                            <v-icon>mdi-certificate</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title class="text-wrap"
                              >Intermediate Python -
                              Nanodegree</v-list-item-title
                            >
                            <v-list-item-subtitle>Udacity</v-list-item-subtitle>
                            <v-list-item-subtitle
                              >January 2022 - Present</v-list-item-subtitle
                            >
                          </v-list-item-content>
                        </v-list-item>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat.
                      </v-expansion-panel-content>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-header expand-icon="mdi-menu-down">
                        <v-list-item three-line>
                          <v-list-item-avatar>
                            <v-icon>mdi-certificate</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title class="text-wrap"
                              >Frontend Web Development -
                              Nanodegree</v-list-item-title
                            >
                            <v-list-item-subtitle>Udacity</v-list-item-subtitle>
                            <v-list-item-subtitle
                              >June 2021 - August 2021</v-list-item-subtitle
                            >
                          </v-list-item-content>
                        </v-list-item>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat.
                      </v-expansion-panel-content>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-header expand-icon="mdi-menu-down">
                        <v-list-item three-line>
                          <v-list-item-avatar>
                            <v-icon>mdi-certificate</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title class="text-wrap"
                              >Fullsatck Web Development -
                              Nanodegree</v-list-item-title
                            >
                            <v-list-item-subtitle>Udacity</v-list-item-subtitle>
                            <v-list-item-subtitle
                              >June 2021 - August 2021</v-list-item-subtitle
                            >
                          </v-list-item-content>
                        </v-list-item>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat.
                      </v-expansion-panel-content>
                    </v-expansion-panel>

                    <v-expansion-panel>
                      <v-expansion-panel-header expand-icon="mdi-menu-down">
                        <v-list-item three-line>
                          <v-list-item-avatar>
                            <v-icon>mdi-certificate</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title
                              >KCSE - Certificate</v-list-item-title
                            >
                            <v-list-item-subtitle
                              >St. Charles Lwanga School, Kitui
                              Kenya</v-list-item-subtitle
                            >
                            <v-list-item-subtitle
                              >February 2013 - December
                              2016</v-list-item-subtitle
                            >
                          </v-list-item-content>
                        </v-list-item>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat.
                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card-text>
              </v-card>
            </v-tab-item>

            <v-tab-item value="work">
              <v-card flat>
                <v-card-text>Work</v-card-text>
              </v-card>
            </v-tab-item>

            <v-tab-item value="experience">
              <v-card flat>
                <v-card-text>Experience</v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs-items>
        </v-card>
      </v-main>
    </v-sheet>
  </v-app>
</template>

<script>
export default {
  name: "App",
  title: "Silas Jimmy",
  created() {
    // Set the theme
    this.appTheme = localStorage.getItem("theme") === "dark";
    this.$vuetify.theme.dark = localStorage.getItem("theme") === "dark";
  },
  data() {
    return {
      appTheme: false,
      tab: "education",
    };
  },
  watch: {
    appTheme(darkTheme) {
      if (darkTheme) {
        this.$vuetify.theme.dark = true;
        localStorage.setItem("theme", "dark");
      } else {
        this.$vuetify.theme.dark = false;
        localStorage.setItem("theme", "light");
      }
    },
  },
};
</script>

<style>
.b {
  border: 1px solid black;
}

html::-webkit-scrollbar {
  display: none;
}
</style>