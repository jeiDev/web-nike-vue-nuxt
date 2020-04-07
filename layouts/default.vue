<template>
  <div>
    <Header />
    <nuxt />
  </div>
</template>

<script>
import Header from '~/components/Default/Header.vue'

export default {
  components: {
    Header
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  color: white;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

li{
  list-style: none;
}

body{
  background-color: black;
}

.margin-box{
  width: 100vw;
  padding-top: 90px;
  padding-left: 130px;
  position: relative;
}
</style>
