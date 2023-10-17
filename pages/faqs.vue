<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="10" lg="10" class="mt-6 mt-lg-10 mt-xl-10 mt-xxl-10 py-6 py-lg-10 py-xl-10 py-xxl-10">
      <v-card variant="tonal" :elevation="0" class="transparent mt-6 mt-lg-16 mt-xl-16 mt-xxl-16">
        <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2">
          <p class="pyas mx-3 my-0">PYAS</p> 常见问题与解答
        </v-card-title>
      </v-card>

      <div class="d-flex justify-center mt-5">
        <ul>
          <li class="my-1" v-for="(item, index) in Faqs" :key="index">
            {{ (index+1) + ". " + item.question }}
            <p>{{ item.answer }}</p>
          </li>
        </ul>
      </div>

      <Footer/>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'FaqsPage',
  data() {
    return {
      Faqs: [
        {
          question: "使用 PYAS 时，遇到安全性提醒，该如何解决？",
          answer: "请确认 PYAS 是从官方网站下载，并点击继续执行，最后给予管理员权限即可。​",
        },
        {
          question: "使用 PYAS 时，该如何更换当前的语言？",
          answer: "请开启 PYAS 主介面，并点击右上角选单内的设置按钮，即可在下方更换当前语言。​",
        },
        {
          question: "使用 PYAS 时，遇到没有回应，该如何解决？",
          answer: "如果 PYAS 正在读取资料，请不要进行其他操作，并耐心等待 PYAS 运行完毕。​",
        },
        {
          question: "使用 PYAS 时，遇到程序崩溃情况，该如何解决？",
          answer: "请在国际官方网站或QQ群(689763963)进行反馈，并标注错误的详细资讯，以便我们更快的修正问题。​",
        },
        {
          question: "使用 PYAS 时，反应速度变慢，该如何解决？",
          answer: "请确保电脑拥有 1GB 以上的內存，并尝试关闭其他影响性能的软件。​",
        },
        {
          question: "使用 PYAS 时，会收集哪些隐私数据？",
          answer: "PYAS 杀毒软件是完全开源的，所以不会收集任何有关用户的隐私数据。​",
        },
        {
          question: "我们对于 PYAS 杀毒软件的定义是什么？",
          answer: "PYAS 属于辅助类杀毒软件，我们仍然在努力守护用户的数据及隐私安全。​",
        },
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
