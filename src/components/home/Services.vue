<template>
  <v-container id="services" tag="section">
    <base-card dark>
      <v-row>
        <v-col cols="12" align="center">
          <base-subheading>My Services</base-subheading>
          <div
            class="col-8"
          >Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</div>
          <v-divider class="col-6"></v-divider>
        </v-col>
        <v-col cols="12" class="d-flex justify-space-around">
          <v-slide-group v-model="model" class="pa-4" center-active show-arrows>
            <v-slide-item
              v-for="item in services"
              :key="item.title"
              v-slot:default="{ active, toggle }"
            >
              <v-card
                max-width="275px"
                class="ma-6"
                :color="active ? 'primary' : ' '"
                @click="toggle"
              >
                <v-img :src="item.img" contain height="150px"></v-img>
                <v-card-title class="justify-center">{{item.title}}</v-card-title>
                <v-card-text class="justify-center">{{item.desc}}</v-card-text>
                <v-card-actions>
                  <v-scale-transition>
                    <v-btn v-if="active" block>Details</v-btn>
                    <v-btn v-else block>Details</v-btn>
                  </v-scale-transition>
                </v-card-actions>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </v-col>
      </v-row>
    </base-card>
  </v-container>
</template>

<script>
export default {
  name: "Services",
  data: () => ({
    model: null,
    services: [
      {
        img: require("@/assets/services/frontend.png"),
        title: "Front-End Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        img: require("@/assets/services/backend.png"),
        title: "Back-End Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        img: require("@/assets/services/uiuxdesaign.png"),
        title: "UI/UX Designer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        img: require("@/assets/services/full-stack-development-main.jpg"),
        title: "Full Stack Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        img: require("@/assets/services/macro-shot-audio-equalizer-744318.jpg"),
        title: "Audio Mix & Mastering",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      }
    ]
  })
};
</script>