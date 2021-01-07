<template>
  <v-container fluid>
    <v-card>
      <div class="title pb-2 text-center">Skills</div>
      <v-divider inset dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">クリックで詳細確認できます</div>
      <v-row justify="space-around">
        <Html />
        <Css />
        <Javascript />
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import Html from '@/components/html.vue';
import Css from '@/components/css.vue';
import Javascript from '@/components/javascript.vue';

export default {
  data () {
    return {
      dialog: false,
    }
  },
  components: {
    Html,
    Css,
    Javascript
  },
}
</script>
