<style scoped>
.mygradient {
  background: linear-gradient(
    53.93deg,
    rgba(0, 0, 0, 100) 45.49%,
    rgba(0, 0, 0, 0) 45.49%
  );
}
</style>
<template>
  <base-card dark>
    <v-img
      :src="require('@/assets/articles/banners.png')"
      class="grey lighten-2"
      height="100%"
      width="100%"
    >
      <div class="fill-height mygradient">
        <v-row class="fill-height pa-4" align="center">
          <v-col cols="12" md="4">
            <v-btn color="primary" depressed>Hello!</v-btn>

            <h1 class="display-1 font-weight-light mt-3">I Am Web Developer</h1>

            <div
              class="body-2 text-lowercase pl-1 mt-3"
            >I'm a Web Developer with extensive for over 5 years. My expertise is to create UI/UX design, full stack web developer, database administrator and many more...</div>
            <div class="mt-3">
              <base-btn
                v-for="(item, i) in items"
                :key="i"
                :href="item.href"
                class="ml-0 mr-3"
                color="primary"
                square
                target="_blank"
              >
                <v-icon v-text="item.icon" />
              </base-btn>
            </div>
          </v-col>
        </v-row>
      </div>
    </v-img>
  </base-card>
</template>

<script>
export default {
  name: "HomeBanner",
  data: () => ({
    items: [
      {
        href: "https://www.instagram.com/snapmyos/",
        icon: "mdi-instagram"
      },
      {
        href: "https://github.com/weynand04/",
        icon: "mdi-github-circle"
      },
      {
        href:
          "https://mail.google.com/mail/?view=cm&fs=1&to=wamaerkabor@gmail.com",
        icon: "mdi-gmail"
      }
    ]
  })
};
</script>
