<template>
  <v-container fluid id="works">
    <v-card>
      <div class="title pb-2 text-center" v-text="title" />

      <v-divider dark />

      <div class="text-subtitle-1 text-center py-2" v-text="description" />
      <v-tabs :value="tab" @change="tab = $event" show-arrows fixed-tabs>
        <v-tab href="#tab-1" class="text-caption" v-text="workTitle.work1" />
        <v-tab href="#tab-2" class="text-caption" v-text="workTitle.work2" />
        <v-tab href="#tab-3" class="text-caption" v-text="workTitle.work3" />
        <v-tab href="#tab-4" class="text-caption" v-text="workTitle.work4" />
      </v-tabs>
      <work-list-item v-model="tab" />
    </v-card>
  </v-container>
</template>

<script>
import WorkListItem from "@/components/work/WorkListItem.vue";
export default {
  data() {
    return {
      title: "Works",
      workTitle: {
        work1: "AueluWeb",
        work2: "Aueluaccounting",
        work3: "Tweetlist",
        work4: "ExaIntern"
      },
      description: "リンクをクリックすることでページに飛びます",
      tab: "tab-1"
    };
  },
  components: {
    WorkListItem
  }
};
</script>
