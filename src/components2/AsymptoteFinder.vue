<script>
export default {
  data() {
    return {
      M: null,
      N: null,
      result: ''
    };
  },
  methods: {
    asymp() {
      const diff = this.M - this.N;

      switch (true) {
        case this.M === this.N:
          this.result = "Asymptote is horizontal";
          break;
        case this.N > this.M:
          this.result = "Asymptote is X axis";
          break;
        case diff === 1:
          this.result = "Linear";
          break;
        case diff === 2:
          this.result = "Quadratic";
          break;
        case diff === 3:
          this.result = "Cubic";
          break;
        case diff === 4:
          this.result = "Quartic";
          break;
        case diff === 5:
          this.result = "Quintic";
          break;
        case diff === 6:
          this.result = "Sextic";
          break;
        case diff === 7:
          this.result = "Septic";
          break;
        case diff === 8:
          this.result = "Octic";
          break;
        case diff === 9:
          this.result = "Nonic";
          break;
        case diff === 10:
          this.result = "Decic";
          break;
        default:
          this.result = "Difference too large";
          break;
      }
    }
  }
};
</script>

<template>
<div class="calc asymp">
    <h3>Asymptote Finder</h3>
    <p>M value</p>
    <input type="number" v-model="M" step="0.001">
    <p>N value</p>
    <input type="number" v-model="N" step="0.001">
    <p>Asymp. type (result)</p>
    <input type="text" :value="result" class="result" readonly>
    <button class="calcbutton" @click="asymp()">Calculate</button>
</div>
</template>

<style scoped>
.asymp {
    background-color: rgb(120, 120, 120);
    position: relative;
    
}
</style>