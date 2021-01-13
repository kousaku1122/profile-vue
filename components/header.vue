<template>
  <v-app-bar color="deep-purple" app clipped-right collapse-on-scroll>
    <v-toolbar-title>PORTFOLIO</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn icon href="https://github.com/kousaku1122">
      <v-icon>mdi-github</v-icon>
    </v-btn>
    <v-app-bar-nav-icon @click="drawerChange"></v-app-bar-nav-icon>
  </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    drawer: true
  }),
  methods: {
    drawerChange() {
      this.drawer != this.drawer;
      this.$emit("drawer", this.drawer);
    }
  }
};
</script>
