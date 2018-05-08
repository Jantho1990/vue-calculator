<template>
  <div class="result-display">
    <span>{{result}}</span>
  </div>
</template>

<style scoped lang="scss">
.result-display {
  border: 1px solid hsl(0, 75%, 50%);
  background: hsl(0, 0%, 25%);
  height: 5em;
  // width: 50%;
  flex: 3 3 auto;
  margin: 0 2.5%;
  span {
    color: hsl(0, 0%, 0%);
    padding: 0.25em 0;
    font-size: 3em;
    width: 100%;
    display: block;
  }
}
</style>

<script>
export default {
  props: ['result']
}
</script>