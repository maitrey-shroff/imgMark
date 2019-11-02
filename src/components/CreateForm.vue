<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex xs6>
        <v-card>
          <v-card-text class="px-0">
            <v-container>
              <v-form v-model="valid">
                <v-layout>
                  <v-flex>
                    <v-text-field
                      v-model="record.ownerid"
                      :rules="urlRules"
                      label="Owner ID test"
                      required
                    ></v-text-field>
                  </v-flex>
                </v-layout>
                <v-flex>
                  <v-text-field v-model="record.owner" label="Owner Name"></v-text-field>
                </v-flex>
                <v-layout>
                  <v-flex>
                    <v-text-field v-model="record.domain" label="Domain"></v-text-field>
                  </v-flex>
                </v-layout>
                <v-layout>
                  <v-flex>
                    <v-text-field v-model="record.imageid" label="Image Name"></v-text-field>
                  </v-flex>
                </v-layout>
                <v-layout>
                  <v-flex>
                    <v-text-field v-model="record.markurl" label="Watermark Logo URL"></v-text-field>
                  </v-flex>
                </v-layout>
                <v-flex xs12 sm4 text-xs-center>
                  <div>
                    <v-btn v-on:click="onSubmit">Upload</v-btn>
                  </div>
                </v-flex>
              </v-form>
              <p>{{ response }}</p>
            </v-container>
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs6>
        <v-card>
          <ImageStack :imageid="record.imageid" width="400" logoWidth="400"/>
          <v-card-text>
            <CodeSample :imageid="record.imageid"/>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>


<script>
import ImageStack from "../components/ImageStack";
import CodeSample from "../components/CodeSample";
export default {
  components: {
    ImageStack,
    CodeSample
  },
  mounted: function() {
    this.$nextTick(function() {
      // Code that will run only after the
      // entire view has been rendered
      //   this.ownerid = "Shutterstock_08232735";
      //   this.owner = "Shutterstock";
      //   this.domain = "http://www.shutterstock.com";
      //   this.imageid = "img01";

      this.record = {
        ownerid: "Shutterstock_08232735",
        owner: "Shutterstock",
        domain: "http://www.shutterstock.com",
        imageid: "img01",
        markurl:
          "https://res.cloudinary.com/filmfest/image/upload/v1549215229/imgmark/logo-flat.png"
      };
    });
  },
  data: function() {
    return {
      response: "",
      record: {
        ownerid: "Shutterstock_08232735",
        owner: "Shutterstock",
        domain: "http://www.shutterstock.com",
        imageid: this.imageid,
        markurl:
          "https://res.cloudinary.com/filmfest/image/upload/v1549215229/imgmark/logo-flat.png"
      }
    };
  },

  methods: {
    onSubmit() {
      this.response = this.imageid;
      this.ImageStack.data.imageid = this.imageid; // || "img01";

      this.record.markurl =
        "`http://res.cloudinary.com/filmfest/image/upload/imgmark/${this.imageid}.png`";
      //   this.CodeSample.data.imageid = this.imageid || "img01";
      //   this.Watermark.data.src = "http://placekitten.com/300/400";
    }
  }
};
</script>

<style>
</style>
