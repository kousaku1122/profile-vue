<template>
  <v-container fluid id="skills">
    <v-card>
      <div class="title pb-2 text-center" v-text="title" />
      <v-divider dark />
      <div class="text-subtitle-1 text-center py-2" v-text="description" />

      <skill-list-item />
    </v-card>
  </v-container>
</template>

<script>
import SkillListItem from "@/components/skill/SkillListItem.vue";

export default {
  data() {
    return {
      title: "Skills",
      description: "クリックで詳細確認できます",
      dialog: false
    };
  },
  components: {
    SkillListItem
  }
};
</script>
