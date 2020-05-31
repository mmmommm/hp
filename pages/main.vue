<template>
  <div>
    <Home/>
    <About/>
    <Skill/>
    <Work/>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import Home from "~/components/container/main/Home.vue";
import About from "~/components/container/main/About.vue";
import Skill from "~/components/container/main/Skill.vue";
import Work from "~/components/container/main/Work.vue";

@Component({
  components: {
    Home,
    About,
    Skill,
    Work,
  }
})
export default class Main extends Vue {
}
</script>