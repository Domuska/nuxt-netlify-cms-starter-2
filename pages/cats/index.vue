<template>
  <div>
    <img :src="imgSrc" />
    <button v-on:click="getImgSrc" class="button--green">Mew!</button>
    <!-- <img src="https://cdn2.thecatapi.com/images/8mu.jpg" /> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgSrc: ""
    };
  },
  // data: {
  //   imgSrc: ''
  // },
  methods: {
    getImgSrc: function(event) {
      console.log("returning image source");
      console.log(this.imgSrc);
      if (this.imgSrc === "" || this.imgSrc === "https://cataas.com/cat") {
        this.imgSrc = "https://cataas.com/cat/black";
      } else {
        this.imgSrc = "https://cataas.com/cat";
      }

      // return 'https://cdn2.thecatapi.com/images/dne.jpg'
      // return this.$store.state.blogPosts
    }
  }
};
</script>