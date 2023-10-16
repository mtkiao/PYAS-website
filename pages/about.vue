<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="10" lg="10" class="mt-6 mt-lg-10 mt-xl-10 mt-xxl-10 py-6 py-lg-10 py-xl-10 py-xxl-10">
      <v-card variant="tonal" :elevation="0" class="transparent mt-6 mt-lg-16 mt-xl-16 mt-xxl-16">
        <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2">
          关于 <p class="pyas mx-3 my-0">PYAS</p> 杀毒软件
        </v-card-title>
      </v-card>

      <div class="d-flex justify-center mt-5">
        <ul>
          <li class="text-h6" v-for="(item, index) in Faqs" :key="index">{{ item }}</li>
        </ul>
      </div>

      <Footer/>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'AboutPage',
  data() {
    return {
      Faqs: [
        "2020年12月17日，PYAS 杀毒软件创立",
        "2021年10月12日，首次在 Github 发布",
        "2022年04月26日，首次加入实时防护",
        "2022年07月28日，查杀率超越部分品牌",
        "2022年08月12日，首次使用PyQt5介面",
        "2023年02月01日，首次在 BiliBili 发布",
        "2023年02月25日，开放云扫毒引擎",
        "2023年05月27日，成功接入360云大脑",
        "2023年06月04日，防御力超越部分品牌",
      ]
    }
  },
}
</script>

<style scoped>
  .pyas {
    font-weight: bold;
    background: -webkit-linear-gradient(45deg, rgb(204, 204, 204) 20%, rgb(134, 134, 134) 90% );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  ul {
    list-style: none;
  }

  ul li {
    font-size: 1.1rem;
  }


</style>
