<template>
  <v-app>
    <v-card
        class="mx-auto overflow-hidden"
        height="400"
        width="100%"
      >
      <Header @drawer="updateDrawer" />
      <Drawer v-model="drawer"/>
      <v-card-text>
        <v-main>
          <v-container>
            <nuxt />
          </v-container>
        </v-main>
      </v-card-text>
    </v-card>
  </v-app>
</template>

<script>
import Header from '@/components/header.vue';
import Drawer from '@/components/drawer.vue';
export default {
  data: () => ({
     drawer: false,
  }),
  components: {
    Header,
    Drawer,
  },
  methods: {
      updateDrawer (value) {
        this.drawer = value
      }
    }
}
</script>
