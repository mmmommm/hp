<template>
  <div>
    <Header/>
      <nuxt />
    <Footer/>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import Header from '../components/presentational/Header.vue'
import Footer from '../components/presentational/Footer.vue'
@Component({
  components: {
    Header,
    Footer
  }
})
export default class Default extends Vue{}
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
}
*{
  margin: 0;
}
</style>
