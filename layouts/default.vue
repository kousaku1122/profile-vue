<template>
  <v-app>
    <v-card class="mx-auto overflow-hidden" width="100%">
      <Header @drawer="updateDrawer" />
      <Drawer @drawer="updateDrawer" v-model="drawer" />

      <v-card-text>
        <v-main>
          <v-container>
            <nuxt />
          </v-container>
        </v-main>
      </v-card-text>
      <Footer />
    </v-card>
  </v-app>
</template>

<script>
import Header from "@/components/header.vue";
import Drawer from "@/components/drawer.vue";
import Footer from "@/components/footer.vue";

export default {
  data: () => ({
    drawer: false
  }),
  components: {
    Header,
    Drawer,
    Footer
  },
  methods: {
    updateDrawer(value) {
      this.drawer = value;
    }
  }
};
</script>
