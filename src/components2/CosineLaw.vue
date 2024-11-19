<script>
export default {
  data() {
    return {
      a: null,
      b: null,
      theta: null,
      result: null
    };
  },
  methods: {
    cosine() {
      if (this.a && this.b && this.theta !== null) {
        const radianTheta = this.theta * (Math.PI / 180);
        this.result = Math.sqrt(
          this.a * this.a + this.b * this.b - 2 * this.a * this.b * Math.cos(radianTheta)
        ).toFixed(3);
      }
    }
  }
};

</script>

<template>
  <div class="calc cosine">
    <h3>Cosine Law</h3>
    <p>Side a</p>
    <input type="number" v-model="a" step="0.001">
    <p>Side b</p>
    <input type="number" v-model="b" step="0.001">
    <p>Angle c</p>
    <input type="number" v-model="theta" step="0.001">
    <p>Side c (result)</p>
    <input type="number" :value="result" class="result" readonly>
    <button class="calcbutton" @click="cosine()">Calculate</button>
  </div>
</template>

<style scoped>
.cosine {
    background-color: rgb(120, 120, 120);
    position: relative;
    margin-top: 0;
}
</style>