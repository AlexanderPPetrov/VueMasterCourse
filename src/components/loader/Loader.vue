<template>
  <div v-show="isLoading" class="loader"></div>
</template>

<script>
  export default {
    computed: {
      isLoading() {
        return this.$store.state.isLoading;
      },
    },
  };
</script>

<style lang="scss">
  $vue-loader: #17a2b8;

  .loader {
    font-size: 10px;
    position: absolute;
    z-index: 9999;
    top: 50%;
    left: 50%;
    margin: -20px 0 0 -20px;
    text-indent: -9999em;
    border-top: 5px solid lighten($vue-loader, 35%);
    border-right: 5px solid lighten($vue-loader, 35%);
    border-bottom: 5px solid lighten($vue-loader, 35%);
    border-left: 5px solid $vue-loader;
    -webkit-transform: translateZ(0);
    -ms-transform: translateZ(0);
    transform: translateZ(0);
    -webkit-animation: loaderSpinner 1.1s infinite linear;
    animation: loaderSpinner 1.1s infinite linear;
    border-radius: 50%;
    width: 40px;
    height: 40px
  }

  @-webkit-keyframes loaderSpinner {
    0% {
      -webkit-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      -webkit-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }
</style>
