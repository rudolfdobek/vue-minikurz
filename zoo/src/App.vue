<script setup>
import PocetNavstevniku from './components/PocetNavstevniku.vue';
import ComputedPromenna from './components/ComputedPromenna.vue';
import DirektivaOn from './components/DirektivaOn.vue';
import DirektivaBind from './components/DirektivaBind.vue';
</script>


<template>
  <div class="container">
    <h1>Zoo</h1>
    <p class="uvod">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui repellat quos, error necessitatibus itaque dignissimos sit, libero debitis est facilis, recusandae delectus voluptate iure maxime. Est quam aperiam incidunt iure.</p>

    <div class="karta">
      <PocetNavstevniku />
    </div>

    <div class="karta">
      <ComputedPromenna />
    </div>

    <div class="karta">
      <DirektivaOn />
    </div>

    <div class="karta">
      <DirektivaBind />
    </div>


  </div>
</template>

<style scoped>
    h1 {
      color: cadetblue;
      text-align: center;
    }

    p.uvod {
      text-align: center;
      font-size: 1.5rem;
      font-weight: bold;
    }

    .karta {
      background-color: coral;
      border-radius: 10px;
      margin: 1rem;
      padding: 2rem;
      font-size: 1.1rem;
      color: white;
    }
</style>