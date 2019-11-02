<template>
  <div class="sidepanel">
    <div>
      <v-btn v-on:click="onSubmit">Download Code</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "CodeSample",
  props: {
    imageid: String
  },
  mounted: function() {
    this.$nextTick(function() {
      this.imageid = this.imageid;
      this.codesnip = "foo bar";
      //    `
      //   <!-- Embed this script into your webpage -->
      //   ${this.imageid}
      //   `;
      // Code that will run only after the
      // entire view has been rendered
    });
  }
};

//codesnip
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sidepanel {
  position: relative;
  top: 30px;
  min-width: 100%;
  min-height: 268px;
  /* background-color: aquamarine; */
}

.codebox {
  min-width: 200%;
  min-height: 240px;
  background-color: white;
}
</style>
