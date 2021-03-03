<template>
  <q-layout view="hHh lpR fFf" class="bg-blue-5">
    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal bordered class="bg-grey-7 text-white text-center shadow-10" style="height: 80px">
      <q-toolbar class="q-pa-md">
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
          </q-avatar>
          VuNAS © {{currentDate}}
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { date } from 'quasar'

const timeStamp = Date.now()
const formattedString = date.formatDate(timeStamp, 'YYYY')

export default {
  name: 'MainLayout',
  data () {
    return {
      currentDate: formattedString
    }
  }
}
</script>
