<template>
  <div id="app">
    <Default>
      <router-view/>
    </Default>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import Default from '../layouts/default.vue'
@Component({
  components: {
    Default
  }
})
export default class Index extends Vue{}
</script>

<style scoped>
*{
  margin: 0;
}
</style>