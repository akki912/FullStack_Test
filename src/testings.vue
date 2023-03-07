<template>
  <div class="heading">
    <h1 style="text-align: center">Convert USD to INR and vice versa</h1>
    <div class="inputConversion">
      <label for="usd-input">Enter USD amount: </label>
      <input type="number" id="usd-input" v-model="usdAmount" />
    </div>
    <div class="intInput">
      <button @click="convertToInr">Convert to INR</button>
      <button @click="convertToUsd">Convert to USD</button>
    </div>
    <div v-if="inrAmount">
      <p>{{ usdAmount }} USD is equivalent to {{ inrAmount }} INR</p>
    </div>
    <div v-if="usdAmount">
      <p>{{ inrAmount }} INR is equivalent to {{ usdAmount }} USD</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      usdAmount: null,
      inrAmount: null,
      conversionRate: 81.84 // 1 USD = 73.98 INR (as of March 2023)
    };
  },
  methods: {
    convertToInr() {
      this.inrAmount = this.usdAmount * this.conversionRate;
    },
    convertToUsd() {
      this.usdAmount = this.inrAmount / this.conversionRate;
    }
  }
};
</script>

<style type="text/css">
.heading {
  margin: 0 auto;
  width: 540px;
}

.inputConversion {
  margin: auto;
  width: 540px;
  text-align: center;
}

.inputConversion.label {
  display: inline-block;
  text-align: center;
}

.intInput {
  margin: auto;
  width: 540px;
  text-align: center;
}
</style>
