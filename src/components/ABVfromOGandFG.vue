<template>
  <h2>ABV from OG and FG</h2>
  <div id="abvogfg">
    <p>
      <label for="og">
        Original gravity
      </label>
      <input type="number" id="og" v-model="og" step=".001">
    </p>
    <p>
      <label for="fg">
        Final gravity
      </label>
      <input type="number" id="fg" v-model="fg" step=".001">
    </p>
    <p>
      {{ message }}
    </p>
    <p>
      <button v-on:click="calcabv">Calculate ABV</button>
    </p>
  </div>
</template>

<script>
export default {
  name: 'ABVfromOGandFG',
  methods: {
    calcabv() {
      const abv = (100 * (og.value - fg.value) / 0.75).toFixed(1);
      this.message = 'The ABV is ' + abv + '%';
    }
  },
  data() {
    return {
      og: 1.05,
      fg: 1.01,
      message: 'Enter gravities then click below'
    }
  },
}
</script>
