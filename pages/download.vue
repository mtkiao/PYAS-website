<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="10" lg="10" class="mt-6 mt-lg-16 mt-xl-16 mt-xxl-16 py-6 py-lg-10 py-xl-10 py-xxl-10">

      <v-card variant="tonal" :elevation="0" class="transparent mt-6 mt-lg-16 mt-xl-16 mt-xxl-16">
        <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2">
          <p class="pyas mx-3 my-0">PYAS</p> 杀毒软件
        </v-card-title>

        <div class="font-weight-black d-flex text-no-wrap justify-center text-h6">
          当前版本: <p class="version my-0 mx-1">{{ PYAS.version }}</p> | 更新日期: {{ PYAS.date }}
        </div>

        <v-card-actions class="mt-2">
          <v-row>
            <v-col cols="12" sm="6" md="6" lg="6" class="d-inline-flex justify-center justify-sm-end justify-md-end">
              <v-btn variant="tonal" class="font-weight-black text-h6 mt-1 white button rounded-pill" style="color: black;" :href="PYAS.downloadLink"> 立即下载➞ </v-btn>
            </v-col>

            <v-col cols="12" sm="6" md="6" lg="6" class="d-inline-flex justify-center justify-sm-start justify-md-start">
              <v-btn variant="tonal" class="font-weight-black text-h6 mt-1 accent button rounded-pill" :href="PYAS.downloadLink2"> 免安装版➞ </v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
      </v-card>

      <Footer/>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'DownloadPage',
  data() {
    return {
      PYAS: {
        version: '2.8.7',
        date: '2023/10/15',
        downloadLink: "https://ghproxy.com/github.com/87owo/PYAS/releases/download/v2.8.7/PYAS_Setup.exe",
        downloadLink2: "https://ghproxy.com/github.com/87owo/PYAS/releases/download/v2.8.7/PYAS.zip",
        githubLink: "https://github.com/87owo/PYAS",
      }
    }
  },
}
</script>

<style scoped>
  .button {
    height: 50px !important;
    width: 150px;
  }

  .pyas {
    font-weight: bold;
    background: -webkit-linear-gradient(45deg, rgb(204, 204, 204) 20%, rgb(134, 134, 134) 90% );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .version{
    font-weight: bold;
    background: -webkit-linear-gradient(45deg, rgb(121, 173, 250) 20%, rgb(243, 181, 255) 90% );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

</style>
