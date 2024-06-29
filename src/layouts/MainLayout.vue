<template>
  <q-layout view="lHh Lpr lFf">
    <q-header :class="headerClass">
      <q-scroll-observer @scroll="onScroll" />
      <q-toolbar>
        <q-toolbar-title>
          PasarKita
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      scrolled: false
    }
  },
  computed: {
    headerClass () {
      return `${this.scrolled ? 'bg-white' : 'bg-transparent'} text-primary`
    }
  },
  methods: {
    onScroll (event) {
      this.scrolled = event.position.top > 10
    }
  }
}
</script>
