<template>
<div class="container">
    <h1>Board meeting</h1>
    <div class="green-circle"></div>
    <div>
    <p class="text">Feb 22 at 6:00 pm</p>
    <p class="text-2">You have been invited to attend the meeting of the Board Directors.</p>
  </div>
</div>
</template>

<script>
export default {
  name: 'CalendarEvent',
}

</script>

<style scoped>
.container {
  background-color: black;
  width: 18.75rem;
  height: 7rem;
  border-radius: 2rem;
  color: white;
  padding: 1rem;
  position: relative;

}

h1 {
  font-size: 0.75rem;
  margin-left: 0.5rem;
}

p {
  font-size: 0.5rem;
  margin-left: 0.5rem;
  color: #656565;
  padding-bottom: -2.5rem;
}
.green-circle {
  background-color: #73c75f !important;
  width: 0.5rem !important;
  height: 0.5rem !important;
  border-radius: 50% !important;
  flex: 1;
  position: absolute;
  top: 2.188rem;
  left: 0.625rem;
}

.text {
  flex: 1;
  flex-direction: column;
  white-space: nowrap;
  margin-bottom: 0.5rem;
  margin-left: 0.5rem;
}

.text-2 {
  margin-top: 0.75rem;
  line-height: 1.5em;
  padding-bottom: 0.5rem;
}
</style>