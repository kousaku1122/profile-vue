<template>
  <v-container fluid>
    <v-card>
      <div class="title pb-2 text-center">Works</div>
      <v-divider inset dark></v-divider>
      <div class="text-subtitle-1 text-center py-2"></div>
      <v-tabs fixed-tabs v-model="tab">
        <v-tab href="#tab-1"> AueluWeb </v-tab>
        <v-tab href="#tab-2"> AueluAccounting</v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <v-tab-item value="tab-1" >
          <v-card flat>
          <v-card-text><AueluWeb /></v-card-text>
        </v-card>

        </v-tab-item>
        <v-tab-item value="tab-2">
          <v-card flat>
          <v-card-text><AueluAccounting /></v-card-text>
        </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </v-container>
</template>

<script>
import AueluWeb from '@/components/aueluweb.vue';
import AueluAccounting from '@/components/aueluaccounting.vue';
export default {
  data() {
    return {
      tab: 'tab-1',
    }
  },
  components: {
    AueluWeb,
    AueluAccounting,
  },
}
</script>
