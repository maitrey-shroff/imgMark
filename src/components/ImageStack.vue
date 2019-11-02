<template>
  <div class="ImageStack">
    <h4>{{message}}</h4>
    <img class="mark" :src="markURL" :width="logoWidth">
    <img class="watermark" :src="watermarkURL" :width="width">
  </div>
</template>

<script>
export default {
  name: "ImageStack",
  data() {
    return {
      message: this.imageid
      // We cache the dimensions of the previous
      // render so that we can clear the area later.
    };
  },

  props: {
    width: String,
    logoWidth: String,
    imageid: String
  },
  mounted: function() {
    this.$nextTick(function() {
      this.message = this.imageid;
      // Code that will run only after the
      // entire view has been rendered
    });
  },
  methods: {
    getBase64Image: function(url) {
      var canvas = document.createElement("canvas");
      canvas.width = 800;
      canvas.height = 600;
      // var canvas = document.getElementById('myCanvas');
      var context = canvas.getContext("2d");

      var mark = new Image();

      mark.src = url;
      // "http://res.cloudinary.com/filmfest/image/upload/t_imgmark-cutter/imgmark/img02.png";

      mark.onload = function() {
        context.drawImage(mark, 0, 0);
        var dataURL = canvas.toDataURL("image/png");
        return dataURL.replace(/^data:image\/(png|jpg);base64,/, "");
      };

      //   var canvas = document.createElement("canvas");
      //   canvas.width = img.width;
      //   canvas.height = img.height;
      //   var ctx = canvas.getContext("2d");
      //   context.drawImage(img, 0, 0);
      //   var dataURL = canvas.toDataURL("image/png");
      //   return dataURL.replace(/^data:image\/(png|jpg);base64,/, "");
    }
  },
  computed: {
    // a computed getter

    watermarkURL: function() {
      // `this` points to the vm instance
      return (
        "https://res.cloudinary.com/filmfest/image/upload/t_imagemark-watermark/v1549190372/imgmark/" +
        this.imageid +
        ".png"
      );
    },
    markURL: function() {
      // `this` points to the vm instance
      let mark =
        "https://res.cloudinary.com/filmfest/image/upload/t_imgmark-cutter/imgmark/" +
        this.imageid +
        ".png";
      //   var base64 = getBase64Image(mark);

      return mark;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ImageStack {
  min-width: 90%;
  min-height: 230px;
}
.logo {
  position: absolute;
  top: 40px;
  left: 5%;
  max-width: 90%;
}

.mark {
  position: absolute;
  top: 40px;
  left: 5%;
  max-width: 90%;
}

.watermark {
  position: absolute;
  top: 40px;
  left: 5%;
  max-width: 90%;
}
</style>
