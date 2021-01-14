<template>
  <v-container fluid id="skills">
    <v-card>
      <div class="title pb-2 text-center">Skills</div>
      <v-divider dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">
        クリックで詳細確認できます
      </div>

      <SkillItems />
    </v-card>
  </v-container>
</template>

<script>
import SkillItems from "@/components/skill-items.vue";

export default {
  data() {
    return {
      dialog: false
    };
  },
  components: {
    SkillItems
  }
};
</script>
