<script>
export default {
  data() {
    return {
      n: null,
      result: null
    };
  },
  methods: {
    gregniz() {
      if (this.n !== null) {
        let sum = 0;
        for (let k = 0; k < this.n; k++) {
          sum += Math.pow(-1, k) / (2 * k + 1);
        }
        this.result = (4 * sum).toFixed(10);
      }
    }
  }
};
</script>

<template>
<div class="calc gregory">
                <h3>Gregniz Pi Approx.</h3>
                <p>N value</p>
                <input type="number" v-model="n">
                <p>Pi approx. (result)</p>
                <input type="number" :value="result" class="result" readonly>
                <button class="calcbutton" @click="gregniz()">Calculate</button>
                
            </div>
</template>

<style scoped>
.gregory {
    background-color: rgb(120, 120, 120);
    position: relative;
    
}
</style>
