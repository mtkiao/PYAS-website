<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="10" lg="10" class="mt-6 mt-lg-16 mt-xl-16 mt-xxl-16 py-6 py-lg-10 py-xl-10 py-xxl-10">

      <v-card variant="tonal" :elevation="0" class="transparent mt-6 mt-lg-16 mt-xl-16 mt-xxl-16">
        <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2">
          万众瞩目的 <p class="pyas mx-3 my-0">PYAS</p> 杀毒软件
        </v-card-title>

        <v-card-text class="font-weight-black d-inline-flex text-center justify-center text-h6 text-lg-h5">
          免费开源、轻巧易用、多重安全防护<br>
          PYAS采用自研本地以及360云端扫毒引擎<br>
          并内置多重系统安全防护，保障数据安全<br>
        </v-card-text>

        <v-card-actions class="mt-2">
          <v-row>
            <v-col cols="12" sm="6" md="6" lg="6" class="d-inline-flex justify-center justify-sm-end justify-md-end">
              <v-btn variant="tonal" class="font-weight-black text-h6 mt-1 accent button rounded-pill" nuxt to="/download"> 立即下载➞ </v-btn>
            </v-col>
            <v-col cols="12" sm="6" md="6" lg="6" class="d-inline-flex justify-center justify-sm-start justify-md-start">
              <v-btn variant="tonal" class="font-weight-black text-h6 mt-1 white button rounded-pill" style="color: black;" href="https://github.com/87owo/PYAS"> <v-img :max-height="40" :max-width="40" src="/links/Github-block.webp" /> Github➞ </v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
        <div class="font-weight-black d-flex text-center justify-center mt-16 text-h6">
          当前版本: <p class="version mx-1 my-0">{{ PYASVersion }}</p>
        </div>
      </v-card>

      <v-card variant="tonal" :elevation="0" class="transparent content-block">
        <div class="d-xxl-flex d-xl-flex d-lg-flex">
          <v-col cols="12" sm="12" md="12" lg="6" xl="6">
            <v-card-title class="font-weight-black text-h3 text-center justify-center justify-lg-center justify-xl-start justify-xxl-start">
              多重系统安全防护
            </v-card-title>

            <v-card-text class="font-weight-black text-h6 justify-center justify-lg-center justify-xl-start justify-xxl-start" style="color: rgb(194, 194, 194)">
              内涵5大系统安全防护，以及81个防护子项目，以及轻便的使用界面，让您拥有无广告、简单和方便的使用体验。<br>
            </v-card-text>

            <ul class="font-weight-bold text-h6 mt-15">
              <li class="my-1" v-for="(item, index) in protects" :key="index">{{ item.title }}: {{ item.subtitle }} </li>
            </ul>
          </v-col>

          <v-divider vertical class="mx-6 d-none d-xl-flex d-xxl-none"></v-divider>
          <v-col cols="12" sm="12" md="12" lg="6" xl="6" class="d-none d-xl-flex d-xxl-none align-center justify-center justify-xl-start justify-xxl-start">
            <v-img class="ms-lg-6 ms-xl-6 ms-xll-6" :max-width="640" :max-height="425" src="/PYAS_UI/PYAS_GUI.png" alt="使用體驗"></v-img>
          </v-col>
          <v-col cols="12" sm="12" md="12" lg="6" xl="6" class="d-none d-lg-flex d-xl-none align-center justify-center justify-xl-start justify-xxl-start">
            <v-img class="ms-lg-6 ms-xl-6 ms-xll-6" :max-width="457" :max-height="287" src="/PYAS_UI/PYAS_GUI_small.png" alt="使用體驗"></v-img>
          </v-col>
        </div>
      </v-card>

      <div class="transparent content-block d-none d-sm-flex">
        <v-carousel cycle>
          <v-carousel-item v-for="(item, index) in pictures" :key="index">
            <div class="font-weight-black d-flex text-center justify-center text-h4 text-lg-h3">{{ item.title }}</div>
            <div class="d-flex text-center justify-center text-h6">{{ item.subtitle }}</div>
            <div class="d-flex justify-center align-center">
              <v-img :max-width="639" :max-height="459" :src="item.src"></v-img>
            </div>
          </v-carousel-item>
        </v-carousel>
      </div>

      <v-card variant="tonal" :elevation="0" class="transparent content-block">
        <v-card-title class="font-weight-black justify-center text-h4 text-lg-h3">
          <p class="pyas mx-3 my-0">PYAS</p> 电脑设备需求
        </v-card-title>

        <v-card-text class="font-weight-black d-inline-flex text-center justify-center text-h6 text-lg-h5">
          最低的系统配置与权限需求
        </v-card-text>

        <v-card-actions class="mt-2">
          <v-row>
            <v-col cols="12" sm="3" md="3" lg="3" class="d-inline-flex justify-center" v-for="(item, index) in systemRequire" :key="index">
              <div>
                <v-img :max-width="200" :max-height="144" :src="item.src"></v-img>
                <p class="font-weight-black text-center justify-center text-h5">{{ item.title }}</p>
                <p class="text-center justify-center text-h6">{{ item.subtitle }}</p>
              </div>
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
  name: 'IndexPage',
  data() {
    return {
      PYASVersion: '2.9.9',
      pictures: [
        {
          title: "电脑状态",
          subtitle: "用户可以在此介面中查看当前电脑状态及安全情况",
          src: "/PYAS_UI/PYAS_Home.png",
        },
        {
          title: "病毒扫描",
          subtitle: "用户可以在此介面中进行病毒扫描及清除恶意文件",
          src: "/PYAS_UI/PYAS_Scan.png",
        },
        {
          title: "实用工具",
          subtitle: "用户可以在此介面中使用这些实用工具来管理电脑",
          src: "/PYAS_UI/PYAS_Tools.png",
        },
        {
          title: "实时防护",
          subtitle: "用户可以在此介面中启用实时防护来保护电脑安全",
          src: "/PYAS_UI/PYAS_Protects.png",
        },
      ],
      protects: [
        {
          title: "进程防护",
          subtitle: "实时扫描系统进程并阻止恶意进程",
        },
        {
          title: "文件防护",
          subtitle: "实时检测文件变化并阻止勒索软件",
        },
        {
          title: "引导防护",
          subtitle: "实时扫描硬盘引导扇区(MBR)并修复",
        },
        {
          title: "注册表防护",
          subtitle: "实时检测高危注册表项目并阻止恶意进程修改",
        },
        {
          title: "网路防护",
          subtitle: "实时检测系统进程是否为远程控制软件并阻止",
        },
      ],
      systemRequire: [
        {
          title: "系统",
          subtitle: "Win 8.1 (64-bit) 及以上",
          src: "/System_require/Windows.webp",
        },
        {
          title: "权限",
          subtitle: "管理员权限",
          src: "/System_require/Defender.webp",
        },
        {
          title: "内存",
          subtitle: "1 GB 或更多",
          src: "/System_require/Ram.webp",
        },
        {
          title: "​硬盘占用",
          subtitle: "1 GB 或更多",
          src: "/System_require/HDD.webp",
        },
      ],
    }
  },
}
</script>

<style scoped>
  .button {
    height: 50px !important;
    width: 150px;
  }

  .introduce-button{
    height: 40px !important;
    width: 140px;
  }

  .pyas {
    font-weight: bold;
    background: -webkit-linear-gradient(45deg, rgb(223, 223, 223) 20%, rgb(189, 189, 189) 90% );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .version{
    font-weight: bold;
    background: -webkit-linear-gradient(45deg, rgb(121, 173, 250) 20%, rgb(243, 181, 255) 90% );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .content-block {
    margin-top: 12%;
  }

</style>
