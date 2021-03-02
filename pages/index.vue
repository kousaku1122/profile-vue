<template>
  <div>
    <About />
    <skill-list />
    <work-list />
  </div>
</template>

<script>
import About from "@/components/about.vue";
import SkillList from "@/components/skill/SkillList.vue";
import WorkList from "@/components/work/WorkList.vue";
export default {
  components: {
    About,
    SkillList,
    WorkList
  }
};
</script>
