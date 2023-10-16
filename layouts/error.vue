<template>
  <v-app dark>
    <v-row justify="center">
      <v-col cols="12" sm="8" md="6">

        <v-card variant="tonal" :elevation="0" class="transparent py-16">
          <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2" v-if="error.statusCode === 404">
            {{ pageNotFound }}
          </v-card-title>
          <v-card-title class="font-weight-black justify-center text-h3 text-lg-h2" v-else>
            {{ otherError }}
          </v-card-title>
        </v-card>

      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: 'EmptyLayout',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: '404 找不到資源',
      otherError: '發生嚴重錯誤',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>

<style scoped>
</style>
