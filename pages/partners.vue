<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="10" md="10" lg="10" class="mt-6 mt-lg-10 mt-xl-10 mt-xxl-10 py-6 py-lg-10 py-xl-10 py-xxl-10">
      <v-card variant="tonal" :elevation="0" class="transparent mt-6 mt-lg-16 mt-xl-16 mt-xxl-16">
        <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2">
          <p class="pyas mx-3 my-0">PYAS</p> 的开发人员
        </v-card-title>

        <v-row>
          <v-col cols="12" xs="12" sm="12" lg="6" class="d-inline-flex justify-center" v-for="(item, index) in Developer" :key="index">
            <div>
              <v-img class="" :max-height="200" :max-width="200" :src="item.avater" :alt="item.name"/>
              <p class="font-weight-black text-center justify-center text-h5 mt-3">{{ item.name }}</p>
              <div class="justify-center d-flex">
                <v-btn variant="tonal" class="font-weight-black text-h6 mt-1 white button rounded-pill" style="color: black;" :href="item.link"> <v-img :max-height="40" :max-width="40" src="/links/Github-block.webp" /> Github➞ </v-btn>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-card>

      <Footer/>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'PartnersPage',
  data() {
    return {
      Developer: [
        {
          name: "PYAS",
          avater: "/avater/PYAS.webp",
          link: "https://github.com/87owo"
        },
        {
          name: "mtkiao",
          avater: "/avater/mtkiao.webp",
          link: "https://github.com/mtkiao"
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

  .content-block {
    margin-top: 12%;
  }

</style>
