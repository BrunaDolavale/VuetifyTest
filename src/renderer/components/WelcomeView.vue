<template>
  <v-layout row wrap justify-center id="wrapper">
    <h1>Hello World</h1>
  </v-layout>
</template>

<script>
  import SystemInformation from './WelcomeView/SystemInformation'

  export default {
    name: 'welcome',
    components: { SystemInformation },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style scoped>
  .centered
  {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .logo
  {
    max-width: 100%;
  }

  .link-btn
  {
    width: 150px;
  }
</style>
