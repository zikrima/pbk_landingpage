<!-- src/components/Navbar.vue -->
<template>
    <q-header>
      <q-toolbar>
        <!-- <q-btn flat round dense icon="menu" aria-label="Menu" @click="toggleLeftDrawer" /> -->
        <q-toolbar-title>Zikri Jersey</q-toolbar-title>
      </q-toolbar>
    </q-header>
  </template>
  
  <script>
  export default {
    data () {
      return {
        leftDrawerOpen: false
      }
    },
    methods: {
      toggleLeftDrawer () {
        this.leftDrawerOpen = !this.leftDrawerOpen
      }
    }
  }
  </script>
  