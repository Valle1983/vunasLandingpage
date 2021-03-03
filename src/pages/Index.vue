<template>
  <q-page class="fullscreen fixed-center background" style="padding-top: 75px">
        <div class="text-h4 text-center bg-grey-3 text-blue-5">
          Willkommen bei VuNAS
        </div>
    <div class="q-pa-md">
      <q-carousel
        animated
        v-model="slide"
        navigation
        infinite
        :autoplay="true"
        arrows
        transition-prev="slide-right"
        transition-next="slide-left"
        @mouseenter="autoplay = false"
        @mouseleave="autoplay = true"
        height="55vh"
      >
        <q-carousel-slide class="cursor-pointer" name="first" @click="myFunction('https://vunasscloud.duckdns.org')" img-src="https://nextcloud.com/media/Nextcloud-Hub-background.png">
          <div class="fixed-center custom-caption">
            <div class="text-h3">VuNAS Cloud</div>
            <div class="text-subtitle1">Deine Cloud</div>
          </div>
        </q-carousel-slide>
        <q-carousel-slide class="cursor-pointer" name="second" @click="myFunction('https://vunasspass.duckdns.org')" img-src="https://store-images.s-microsoft.com/image/apps.9037.15bced16-76b6-40f0-b229-b0fa0f565ba8.ce68633c-0cdb-41c0-b52e-db9ec3f09809.7968cb41-a4a0-4278-86d8-7bc876fa5431">
          <div class="fixed-center custom-caption">
            <div class="text-h3">Bitwarden</div>
            <div class="text-subtitle1">Passwörter Verwalten</div>
          </div>
        </q-carousel-slide>
        <q-carousel-slide class="cursor-pointer" name="third" @click="myFunction('https://vunasswiki.duckdns.org')" img-src="https://www.amagoo.com/fileadmin/images/Inhaltsbilder/Atlassian/atlassian_products.jpeg">
          <div class="fixed-center custom-caption">
            <div class="text-h3">Jira Confluence</div>
            <div class="text-subtitle1">Wiki</div>
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </q-page>
</template>

<script>

export default {
  data () {
    return {
      slide: 'first'
    }
  },
  methods: {
    myFunction: function (link) {
      window.open(link, '_blank')
    }
  }
}
</script>
<style lang="sass" scoped>
.background
  background-image: url("../assets/download.png")
  height: 100%
  width: 100%
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3)
</style>
