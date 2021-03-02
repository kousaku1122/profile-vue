<template>
  <div>
    <About />
    <Skills />
    <work-list />
  </div>
</template>

<script>
import About from "@/components/about.vue";
import Skills from "@/components/skills.vue";
import WorkList from "@/components/work/WorkList.vue";
export default {
  components: {
    About,
    Skills,
    WorkList
  }
};
</script>
