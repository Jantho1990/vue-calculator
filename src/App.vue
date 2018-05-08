<template>
  <div id="app">
    <div class="row">
      <ResultDisplay result="0"/>
      <CalcButton face="Œ"/>
    </div>
    <div class="row">
      <CalcButton face="1"/>
      <CalcButton face="2"/>
      <CalcButton face="3"/>
      <CalcButton face="+"/>
    </div>
    <div class="row">
      <CalcButton face="4"/>
      <CalcButton face="5"/>
      <CalcButton face="6"/>
      <CalcButton face="−"/>
    </div>
    <div class="row">
      <CalcButton face="7"/>
      <CalcButton face="8"/>
      <CalcButton face="9"/>
      <CalcButton face="✕"/>
    </div>
    <div class="row">
      <CalcButton face="⌫"/>
      <CalcButton face="0"/>
      <CalcButton face="="/>
      <CalcButton face="÷"/>
    </div>
  </div>
</template>

<script>
import math from 'mathjs'
import CalcButton from './components/CalcButton'
import ResultDisplay from './components/ResultDisplay'

export default {
  name: 'VueCalculator',
  components: {
    CalcButton,
    ResultDisplay
  },
  data: {
    display: 0,
    equation: '',
    result: 0
  },
  methods: {
    appendToEquation (v) {
      this.equation += v
    },
    parseEquation () {
      this.result = math.eval(equation)
    },
    updateDisplay (v) {
      if (!isNaN(v)) {
        this.display = v
      }
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 580px;
  margin: 60px auto 0;
  background: hsl(0deg, 0%, 5%);
  font-size: 1rem;
  .row {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: 1rem 0;
    &:first-child {
      // padding: 0 0 1rem;
    }
  }
}
</style>
