<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="quasar-gcp">
      <q-toolbar>
        <q-toolbar-title class='quasar-gcp--template-header-font'>
          <router-link to="/">Quasar's Firebase & Cloud Firestore Template</router-link>
        </q-toolbar-title>

        <user-menu></user-menu>
        <!-- <q-tabs>
          <q-route-tab
            slot="title"
            icon="map"
            to="/your/route"
            replace
            label="One Tab"
          />
          <q-route-tab
            slot="title"
            icon="assignment"
            to="/some/other/route"
            replace
            label="Other Tab"
          />
        </q-tabs> -->
      </q-toolbar>
    </q-header>

    <q-page-container>
      <!-- This is where pages get injected -->
      <router-view />
    </q-page-container>
    <customFooter></customFooter>
  </q-layout>
</template>

<script>
import customFooter from '../components/CustomFooter.vue'
import { openURL } from 'quasar'
import userMenu from '../components/UserMenu.vue'

export default {
  name: 'Basic',
  components: {
    customFooter,
    userMenu
  },
  data () {
    return {
      leftDrawer: false
    }
  },
  methods: {
    openURL
  }
}
</script>

<style lang='stylus'>
</style>
