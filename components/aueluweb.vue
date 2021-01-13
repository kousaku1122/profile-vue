<template>
  <v-container>
    <v-img :src="image_src" eager></v-img>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      image_src: require("@/assets/image/aueluweb.png")
    };
  }
};
</script>
