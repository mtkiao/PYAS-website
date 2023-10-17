<template>
  <v-app dark>
    <v-app-bar fixed app scroll-behavior="hide" scroll-threshold="100" class="nav">
      <span class="d-inline-flex align-center">
        <a href="/" class="d-inline-flex align-center text-decoration-none">
          <v-img max-height="50" max-width="50" class="rounded-circle mr-2" src="/icon/PYAS_white.webp"></v-img>
          <v-toolbar-title class="font-weight-black" style="color: white">{{ title }}</v-toolbar-title>
        </a>
      </span>
      <v-spacer />
      <v-btn variant="text" class="font-weight-black rounded-xl mx-1" nuxt to="/"> 主頁 </v-btn>
      <v-btn variant="text" class="font-weight-black rounded-xl mx-1 d-none d-sm-flex" nuxt to="/download"> 下载 </v-btn>
      <v-btn variant="text" class="font-weight-black rounded-xl mx-1 d-none d-sm-flex" nuxt to="/faqs"> 常见问题 </v-btn>
      <v-btn variant="text" class="font-weight-black rounded-xl mx-1" nuxt to="/partners"> 合作伙伴 </v-btn>
      <v-btn variant="text" class="font-weight-black rounded-xl mx-1" nuxt to="/about"> 关于 </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
export default {
  name: 'PYAS',
  data() {
    return {
      title: 'PYAS',
    }
  },
}
</script>

<style scoped>
  .nav {
    padding-left: 2%;
    padding-right: 2%;
  }
  @media(max-width: 1280px) {
    .nav {
      padding-left: 10%;
      padding-right: 10%;
    }
  }
  @media(max-width: 720px) {
    .nav {
      padding-left: 0;
      padding-right: 0;
    }
  }
</style>
