<template>
  <div class="container p-4">
    <h1><b>Revenue</b></h1>
    <p>Last 7 days VS prior week</p>
  <img src="../assets/images/chart.jpg">
</div>
</template>


<script>
export default {
  name: 'LineChart',
}
</script>


<style scoped>
.container {
  border-radius: 1.25rem;
  border: none;
  background-color: #d0e1e9 !important;
}

img {
  display: block;
  height: 80%;
  width: 100%;
}

h1 {
  font-size: 1rem;
}

p {
  font-size: 0.75rem;
  float: right;
  margin-top: -1.5rem;
}
</style>

