<template>
  <div id="home">
    <articles>
      <banner />
    </articles>

    <about />

    <services />

    <subscribe />
  </div>
</template>

<script>
export default {
  name: "Home",

  components: {
    About: () => import("@/components/home/About"),
    Articles: () => import("@/components/home/Articles"),
    Banner: () => import("@/components/home/Banner"),
    Subscribe: () => import("@/components/home/Subscribe"),
    Services: () => import("@/components/home/Services")
  }
};
</script>
