<template>
  <div id='app'>
    <Home/>
    <About/>
    <Skill/>
    <Work/>
  </div>
</template>

<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import Home from '~/components/container/Home.vue';
import About from '~/components/container/About.vue';
import Skill from '~/components/container/Skill.vue';
import Work from '~/components/container/Work.vue';
@Component({
  components: {
    Home,
    About,
    Skill,
    Work
  }
})
export default class Index extends Vue{}
</script>
<style scoped>
*{
  margin: 0;
}
</style>