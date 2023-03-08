<template>
  <!-- <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-indigo-9 text-white">
      <q-toolbar>
        <q-toolbar-title>
          Plast Polimer Product
        </q-toolbar-title>
        <div class="text-h6"><a href="tel:+998933338575" style="color: white;">
            +xxx xx xxx xxxx
          </a></div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout> -->

  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-indigo-9 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <!-- <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar> -->
          Plast Polimer Product
        </q-toolbar-title>
        <q-tabs align="right">
          <q-route-tab to="/page1" label="Home" />
          <q-route-tab to="/gallery" label="Gallery" />
          <q-route-tab to="/contact" label="Contact us" />
        </q-tabs>
      </q-toolbar>

    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'



export default defineComponent({
  name: 'MainLayout',

  setup() {
    return {}
  }
})
</script>

<style lang="sass" scoped>
.tabs
  color: white
  
</style>