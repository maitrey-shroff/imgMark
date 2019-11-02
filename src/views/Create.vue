<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card class="card">
          <!-- <v-card-text class="px-500"> -->
          <CreateForm/>
          <!-- </v-card-text> -->
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>


<script>
import CreateForm from "../components/CreateForm";
import ImageStack from "../components/ImageStack";

export default {
  components: {
    CreateForm,
    ImageStack
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  min-height: 400px;
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


<script>
import CreateForm from "../components/CreateForm";
import ImageStack from "../components/ImageStack";

export default {
  components: {
    CreateForm,
    ImageStack
  }
};
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
