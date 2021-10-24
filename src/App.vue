<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import FeatureList from './components/FeatureList.vue';
import ABVfromOGandFG from './components/ABVfromOGandFG.vue';
import ABVfromSGandBrix from './components/ABVfromSGandBrix.vue';
</script>

<template>
  <h1><router-link to="/">James Brewing</router-link></h1>
  <main>
    <router-view />
  </main>
</template>

<style>
body {
    text-align: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
div {
    margin: 10px;
}
label {
    display: block;
}
input {
    width: 10ch;
}
a {
    color: black;
}
h1 > a {
    text-decoration: none;
}
</style>
