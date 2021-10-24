<template>
  <h2>Strike Water Temperature</h2>
  <div id="strikewater">
    <div>
      <label for="malt">
        Malt temperature
      </label>
      <input type="number" id="malt" v-model="malt">
    </div>
    <div>
      <label for="target">
        Target temperature
      </label>
      <input type="number" id="target" v-model="target">
    </div>
    <div>
      <label for="ratio">
        Water to malt ratio
      </label>
      <input type="number" id="ratio" v-model="ratio" step=".1">
    </div>
    <div>
      Strike water temperature is {{ strikeWater }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'StrikeWater',
  data() {
    return {
      malt: 55,
      target: 152,
      ratio: 1.4
    }
  },
  computed: {
    strikeWater() {
      return (0.2 / this.ratio * (this.target - this.malt) + Number(this.target)).toFixed(1);
    }
  }
}
</script>
