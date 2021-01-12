<template>
  <v-container fluid>
    <v-card>
      <div class="title pb-2 text-center">Works</div>
      <v-divider inset dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">
        リンクをクリックすることでページに飛びます
      </div>
      <v-tabs fixed-tabs v-model="tab">
        <v-tab href="#tab-1"> AueluWeb </v-tab>
        <v-tab href="#tab-2"> AueluAccounting</v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <v-tab-item value="tab-1" eager>
          <v-card flat>
            <v-btn
              rounded
              href="https://www.teamauelu.me/"
              min-width="100%"
              style="text-transform: none"
              class="mt-3 mb-2"
            >
              <v-icon style="text-align: right;">mdi-lock</v-icon>
              https://www.teamauelu.me/
            </v-btn>
            <v-container
              id="scroll-target"
              style="max-height: 500px"
              class="overflow-y-auto"
            >
              <AueluWeb />
            </v-container>
          </v-card>
        </v-tab-item>
        <v-tab-item value="tab-2" eager>
          <v-card flat>
            <v-btn
              rounded
              href="https://aueluaccounting.herokuapp.com/"
              min-width="100%"
              style="text-transform: none"
              class="mt-3 mb-2"
            >
              <v-icon style="text-align: right;">mdi-lock</v-icon>
              https://aueluaccounting.herokuapp.com/
            </v-btn>
            <v-container
              id="scroll-target"
              style="max-height: 500px"
              class="overflow-y-auto"
            >
              <AueluAccounting />
            </v-container>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </v-container>
</template>

<script>
import AueluWeb from "@/components/aueluweb.vue";
import AueluAccounting from "@/components/aueluaccounting.vue";
export default {
  data() {
    return {
      tab: "tab-1"
    };
  },
  components: {
    AueluWeb,
    AueluAccounting
  }
};
</script>
