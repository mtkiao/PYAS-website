<template>
  <div>
    <div class="transparent content-block justify-center d-flex">
      <form v-for="(item, index) in links" :key="index">
        <button class="transparent mx-2" :formaction="item.href"><v-img :max-height="50" :max-width="50" :src="item.icon" /></button>
      </form>
    </div>
    <div class="transparent text-decoration-underline justify-center d-flex mt-5">
      ©2020-2023 PYAS, 由 PYDT 创建
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        {
          icon: "/links/Github.webp",
          href: "https://github.com/87owo/PYAS"
        },
        {
          icon: "/links/Discord.webp",
          href: "https://discord.gg/4ktutUCDN9"
        },
        {
          icon: "/links/Youtube.webp",
          href: "https://www.youtube.com/@pyas"
        },
        {
          icon: "/links/Bilibili.webp",
          href: "https://space.bilibili.com/1060500587"
        },
      ]
    }
  },
}
</script>

<style scoped>
  .content-block {
    margin-top: 12%;
  }
</style>
