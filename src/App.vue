<template>
  <div id="app">
    <Slideout v-if="menuOpen"/>
    <MenuButton @toggle-menu="toggleMenu"/>
  </div>
</template>

<script>
import Slideout from './components/Slideout.vue'
import MenuButton from './components/MenuButton.vue'

export default {
  name: 'app',
  data() {
    return {
      menuOpen: true
    }
  },
  components: {
    Slideout,
    MenuButton
  },
  methods: {
    toggleMenu () {
      this.menuOpen = !this.menuOpen
    }
  }
}
</script>

<style lang="scss">
html {
  margin: 0;
  padding: 0;
}

body {
  margin: 0;
  padding: 0;
}
h1, h2, h3, h4, h5 {
  padding: 0;
  margin: 0;
}
#app {
  display: flex;
  margin: 0;
  padding: 0;
}
</style>
