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
      The ABV is {{ abv }}%
    </p>
  </div>
</template>

<script>
export default {
  name: 'ABVfromOGandFG',
  data() {
    return {
      og: 1.05,
      fg: 1.01
    }
  },
  computed: {
    abv() {
      return (100 * (this.og - this.fg) / 0.75).toFixed(1);
    }
  }
}
</script>