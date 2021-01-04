<template>
  <v-container fluid>
    <v-card>
      <div class="title pb-2 text-center">Skills</div>
      <v-divider inset dark></v-divider>
      <div class="text-subtitle-1 text-center py-2">クリックで詳細確認できます</div>
      <v-row justify="space-around">
        <v-col cols="6" md="3" class="text-center">
          <v-hover v-slot="{ hover }">
            <v-card  :elevation="hover ? 12 : 2">
              <v-dialog
              width="500"
              >
              <template v-slot:activator="{ on, attrs }">
                <v-img
                :src="html_image_src"
                v-bind="attrs"
                v-on="on"
                ></v-img>
              </template>
              <template v-slot:default="dialog">
                <v-card>
                  <v-toolbar
                  color="primary"
                  dark
                  >HTML5</v-toolbar>
                  <v-card-text>
                    <div class="text-body-1 pa-12">Hello world!</div>
                  </v-card-text>
                  <v-card-actions class="justify-end">
                    <v-btn
                    text
                    @click="dialog.value = false"
                    >Close</v-btn>
                  </v-card-actions>
                </v-card>
              </template>
            </v-dialog>
            <v-divider></v-divider>
            <p>HTML5</p>
          </v-card>
        </v-hover>
      </div>
    </v-col>
  </v-row>
</v-card>
</v-container>
</template>

<script>
export default {
  data () {
    return {
      dialog: false,
      html_image_src: require("@/assets/image/html.png"),
    }
  },
}
</script>
