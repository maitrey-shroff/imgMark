<template>
  <div class="about">
    <v-container>
      <v-layout text-xs-left wrap>
        <v-flex xs12>
          <v-img class="aboutImage" :src="require('../assets/about.jpg')" contain width="1200"></v-img>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>


<script>
export default {};
</script>
<style>
.aboutImage {
  text-align: "center";
}
</style>
