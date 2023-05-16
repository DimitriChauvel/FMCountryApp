<template>
  <main>
    <pre v-for="country in countries" v-bind:key="country.name.common">
      country: <span>{{ country.name.common }}</span>
      region: <span>{{ country.region }}</span>
      capital: <span v-for="capital in country.capital" v-bind:key="capital">{{ capital }}</span>
      flag-url: <a v-bind:href="country.flags.svg">{{ country.flags.alt }}</a>
    </pre>
  </main>
</template>

<script setup>
  import { ref } from 'vue'

  const countries = ref([])

  fetch('https://restcountries.com/v3.1/all')
    .then((response) => response.json())
    .then((data) => countries.value = data)
</script>
