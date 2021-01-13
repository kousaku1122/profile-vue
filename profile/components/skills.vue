<template>
  <v-container fluid id="skills">
    <v-card>
      <div class="title pb-2 text-center">Skills</div>
      <v-divider dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">
        クリックで詳細確認できます
      </div>
      <v-row justify="space-around">
        <Html />
        <Css />
        <Javascript />
        <Vue />
        <Ruby />
        <C />
        <Java />
        <Excel />
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import Html from "@/components/html.vue";
import Css from "@/components/css.vue";
import Javascript from "@/components/javascript.vue";
import Vue from "@/components/vue.vue";
import Ruby from "@/components/ruby.vue";
import C from "@/components/c.vue";
import Java from "@/components/java.vue";
import Excel from "@/components/excel.vue";

export default {
  data() {
    return {
      dialog: false
    };
  },
  components: {
    Html,
    Css,
    Javascript,
    Vue,
    Ruby,
    C,
    Java,
    Excel
  }
};
</script>
