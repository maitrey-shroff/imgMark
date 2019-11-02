<template>
  <v-container>
    <v-layout text-xs-left wrap>
      <v-flex xs12>
        <v-img :src="require('../assets/logo.png')" contain height="300"></v-img>
      </v-flex>

      <v-flex mb-4>
        <br>
        <br>
        <br>
        <h1 class="display-2 font-weight-bold mb-3">Welcome to imgMark</h1>
        <h2 class="subheading font-weight-regular">
          imgMARK is an image rights protection service that
          enables high quality unmarked images to be displayed on authenticated sites, and any unauthorized downloads will be automatically watermarked.
        </h2>
      </v-flex>
      <v-flex xs12>
        <v-img :src="require('../assets/how.jpg')" width="900"></v-img>
        <br>
        <br>
        <br>
        <h1 class="display-2 font-weight-bold mb-3">Coming Soon Mobile Application Support</h1>
        <br>
        <h2
          class="subheading font-weight-regular"
        >imgMARK Mobile will address image rights protection on the go!</h2>
        <br>
        <v-img :src="require('../assets/rights.png')" width="300"></v-img>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
</style>
