<style scoped>
.mygradient {
  background: linear-gradient(
    50.2deg,
    rgba(255, 255, 255, 100) 71.69%,
    rgba(0, 0, 0, 0) 71.71%
  );
}
</style>
<template>
  <v-container id="about" tag="section">
    <base-card dark>
      <v-img
        :src="require('@/assets/articles/banners2.png')"
        class="grey lighten-2"
        height="70%"
        width="100%"
        contain
      >
        <div class="fill-height mygradient">
          <v-row class="fill-height pa-4 black--text" align="center">
            <v-col cols="12" md="8">
              <base-subheading>About Me</base-subheading>
              <p>I'm a freelancer Web Developer having 5 years. of expertise.</p>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
              <v-row>
                <v-col cols="12" md="6">
                  <v-list disabled dense light>
                    <v-list-item-group>
                      <v-list-item v-for="item in items" :key="item.title">
                        <v-list-item-icon>
                          <v-icon>{{item.icon}}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-content>
                          <v-list-item-title>{{item.text}}</v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list-item-group>
                  </v-list>
                </v-col>
                <v-col cols="12" md="6">
                  <v-list disabled dense light>
                    <v-list-item-group>
                      <v-list-item v-for="item in items2" :key="item.title">
                        <v-list-item-icon>
                          <v-icon>{{item.icon}}</v-icon>
                        </v-list-item-icon>
                        <v-list-item-content>
                          <v-list-item-title>{{item.text}}</v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list-item-group>
                  </v-list>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </div>
      </v-img>
    </base-card>
  </v-container>
</template>

<script>
export default {
  name: "HomeAbout",
  data: () => ({
    items: [
      { text: "Phone  : 0921-25021", icon: "mdi-phone" },
      { text: "Lokasi : Waupnor, Biak Kota", icon: "mdi-map-marker" }
    ],
    items2: [
      { text: "Age    : 23", icon: "mdi-calendar-range" },
      { text: "Email  : wamaerkabor@gmail.com", icon: "mdi-gmail" }
    ]
  })
};
</script>
