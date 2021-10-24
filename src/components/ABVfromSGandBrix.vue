<template>
  <h2>ABV from SG and Brix</h2>
  <div id="abvsgbrix">
    <p>
      <label for="sg">
        Specific gravity
      </label>
      <input type="number" id="sg" v-model="sg" step=".001">
    </p>
    <p>
      <label for="brix">
        Brix
      </label>
      <input type="number" id="brix" v-model="brix" step=".1">
    </p>
    <p>
      The ABV is {{ abv }}%
    </p>
  </div>
</template>

<script>
export default {
  name: 'ABVfromSGandBrix',
  data() {
    return {
      sg: 1.01,
      brix: 8,
      message: 'Enter gravity and brix then click below'
    }
  },
  computed: {
    abv() {
      return (1.646 * this.brix - 2.703 * (145 - 145 / this.sg) - 1.794).toFixed(1);
    }
  }
}
</script>
