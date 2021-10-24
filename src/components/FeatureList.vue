<template>
  <nav>
    <p>
      <router-link to="/abvogfg">ABV from OG and FG</router-link>
    </p>
    <p>
      <router-link to="/abvsgbrix">ABV from SG and Brix</router-link>
    </p>
    <div>
      <router-link to="/strikewater">Strike Water Temperature</router-link>
    </div>
  </nav>

</template>

<script>
export default {
  name: 'FeatureList'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
