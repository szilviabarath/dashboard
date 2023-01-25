<template>
    <div class="container col-2 p-2">
        <h1 class="pt-2 mt-1"><b>Formation status</b></h1>
         <p>In progress</p>
         <progress id="progress-bar" value="70" max="100"></progress>
         <br>
         <p class="text-center"><b>Estimated processing</b></p>
         <p class="text-center align">4-5 business days</p>
         <button class="btn bg-light"><b>View status</b></button>
    </div>
</template>

<script>
export default {
  name: 'FormationStatus',
}
</script>

<style scoped>
.container {
  margin-top: 7rem;
}

div {
  border-radius: 1.9rem;
  background-color: black;
  width: 20rem;
  height: 17rem;
  color: white;
  padding: 0.5rem;
}

h1 {
  font-size: 1.3rem;
  margin-left: 0.5rem;
}

p {
  font-size: 0.75rem;
}

p:not(.text-center) {
  margin-left: 0.5rem;
}

progress {
  border-radius: 0.5rem;
  background-color: #404040;
  width: 80%;
  display: flex;
  margin: 0 auto;
}

progress::-webkit-progress-bar {
  border-radius: 0.5rem;
  background-color: #404040;
  display: flex;
  margin: 0 auto;
}

progress::-webkit-progress-value {
  background-color: white;
  border-radius: 0.5rem;
}

progress::-moz-progress-bar {
  border-radius: 10px.5rem;
  background-color: #404040;
  display: flex;
  margin: 0 auto;
}

button {
  display: flex;
  margin: 0 auto;
  width: 80%;
  justify-content: center;
  font-size: 0.75rem;
}
.align {
  margin-top: -0.75rem;
}
</style>
