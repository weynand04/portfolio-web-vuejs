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
        <v-col
          v-for="item in services"
          :key="item.title"
          cols="12"
          sm="4"
          class="d-flex justify-space-around"
        >
          <v-card max-width="274px" dark>
            <v-img :src="require('@/assets/services/html_tag.png')" contain height="150px"></v-img>
            <v-card-title class="justify-center">{{item.title}}</v-card-title>
            <v-card-text class="justify-center">{{item.desc}}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </base-card>
  </v-container>
</template>

<script>
export default {
  name: "Services",
  data: () => ({
    services: [
      {
        title: "Front-End Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        title: "Back-End Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      },
      {
        title: "Full stack Developer",
        desc:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s."
      }
    ]
  })
};
</script>