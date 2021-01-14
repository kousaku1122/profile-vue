<template>
  <v-container fluid id="works">
    <v-card>
      <div class="title pb-2 text-center">Works</div>
      <v-divider dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">
        リンクをクリックすることでページに飛びます
      </div>
      <v-tabs :value="tab" @change="tab = $event" show-arrows fixed-tabs>
        <v-tab href="#tab-1" class="text-caption"> AueluWeb </v-tab>
        <v-tab href="#tab-2" class="text-caption"> AueluAccounting</v-tab>
      </v-tabs>
      <Work v-model="tab" />
    </v-card>
  </v-container>
</template>

<script>
import Work from "@/components/work.vue";
export default {
  data() {
    return {
      tab: "tab-1"
    };
  },
  components: {
    Work
  }
};
</script>
