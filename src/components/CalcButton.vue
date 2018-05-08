<template>
  <div class="calc-button">
    <button>{{face}}</button>
  </div>
</template>

<style scoped lang="scss">
.calc-button {
  width: 20%;
  padding: 0 2.5%;
  height: 5em;
  margin: auto;
  button {
    width: 100%;
    height: 100%;
    border: none;
    border-radius: 0;
    font-size: 3em;
  }
}
</style>

<script>
export default {
  props: ['face']
}
</script>