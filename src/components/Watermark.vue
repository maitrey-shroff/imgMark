<template>
  <div class="watermark">
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>
        <v-flex xs6>
          <v-card>
            <v-card-text class="logo">
              <img alt="Vue logo" class="watermark" :src="src" :width="width">
              <img alt="Vue logo" class="mark" :src="mark" :width="logoWidth">
            </v-card-text>
          </v-card>
        </v-flex>
        <!-- <v-flex xs6>
          <v-card>Response</v-card>
        </v-flex>-->
      </v-layout>
    </v-container>
    <div class="logox"></div>
    <!-- <h1>
      {{ width }}
      <br>
      {{mark}}
      <br>
      {{src}}
      <br/>
      {{logoWidth}}
    </h1>-->
  </div>
</template>

<script>
export default {
  name: "Watermark",
  props: {
    width: String,
    src: String,
    mark: String,
    logoWidth: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo {
  position: absolute;
  top: 0px;
  left: 0px;
}

.mark {
  position: absolute;
  top: 280px;
  left: 280px;
}

.watermark {
  position: absolute;
  top: 0px;
  left: 0px;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
