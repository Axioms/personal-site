<template>
  <div class="grid grid-cols-3 gap-8 container mx-auto bg-white dark:bg-gray-900">
    <li v-for="n in 10">
      <TestComp class="" />
    </li>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  
})
</script>