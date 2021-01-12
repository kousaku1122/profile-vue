<template>
  <div>
    <About />
    <Skills />
    <Works />
  </div>
</template>

<script>
import About from "@/components/about.vue";
import Skills from "@/components/skills.vue";
import Works from "@/components/works.vue";
export default {
  components: {
    About,
    Skills,
    Works
  }
};
</script>
