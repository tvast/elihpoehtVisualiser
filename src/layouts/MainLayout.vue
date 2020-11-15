<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title to="/visualizer">
          Elihpoeht
        </q-toolbar-title>

      </q-toolbar>
        <q-tabs>
  <q-route-tab
    icon="mail"
    to="/visualizer"
    exact
  />
  <q-route-tab
    icon="alarm"
    to="/alarms"
    exact
  />
</q-tabs>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: true
    }
  }
}
</script>
