<template>
  <div class="about">
    <h1>
      This page is <span class="flip-word">{{ word }}</span>
    </h1>
  </div>
</template>

<script>
export default {
  name: 'AboutView',
  components: {},
  computed: {
    word() {
      return this.$route.params.word.toUpperCase();
    },
  },
};
</script>

<style scoped>
.flip-word {
  display: inline-block;
  font-family: cursive;
  font-style: italic;
  font-size: 40px;
  animation-name: groovy;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
@keyframes groovy {
  0% {
    color: pink;
    transform: rotate3d(1, 1, 1, -12deg);
  }
  50% {
    color: lightblue;
    transform: rotate3d(1, 1, 1, 12deg);
  }
  100% {
    color: pink;
    transform: rotate3d(1, 1, 1, -12deg);
  }
}
</style>
