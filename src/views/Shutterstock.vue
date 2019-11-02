
<template>
  <div>
    <v-layout>
      <v-spacer width="50" height="10"/>
      <v-flex xs4>
        <img
          src="https://res.cloudinary.com/filmfest/image/upload/c_scale,e_make_transparent:10,w_300/v1549225360/imgmark/shutterstock.png"
        >
      </v-flex>
    </v-layout>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img01" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img02" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>

        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img03" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img04" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img05" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>

        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img06" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img07" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img08" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>

        <v-flex xs4>
          <v-card>
            <v-card-text class="px-200">
              <ImageStack imageid="img09" width="400" logoWidth="400"/>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import ImageStack from "../components/ImageStack";

export default {
  components: {
    ImageStack
  }
};
</script>

<style scoped>
.row {
  min-height: 200px;
}
.mark {
  position: absolute;
  top: 400px;
  left: 800px;
  width: 400px;
  /* push */
}
.watermark {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 1200px;
  /* push */
}
</style>