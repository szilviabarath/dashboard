<template>

      <div class="wrapper">
        <h1><b>Your to-Do list</b></h1>
    <div class="container d-flex" v-for="item in items" :key="item.title">
    <div class="icon-container">
        <i :class="'fa fa-' + item.icon"></i>
</div>
<br>
<br>
<div class="text-container">
    <h2><b>{{ item.title }}</b></h2>
    <p>{{ item.date }}</p>
</div>
</div>
</div>

</template>

<script>

export default {
  name: 'ToDoList',
    data() {
      return {
        items: [
          {
            icon: "square",
            title: "Run payroll",
            date: "Mar 4 at 6:00 pm"
          },
          {
            icon: "circle",
            title: "Review time off request",
            date:"Mar 7 at 6:00 pm"
          },
          {
            icon: "square",
            title: "Sign board resolution",
            date:"Mar 12 at 6:00 pm"
          },
          {
            icon: "square",
            title: "Finish onboarding Tony",
            date:"Mar 12 at 6:00 pm"
          }
        ]
      };

    }
}
</script>

<style scoped>
.wrapper {
    border-radius: 1.25rem;
    border: none;
    padding: 0.5rem;
    margin-left: 0.9rem;
}

h1 {
    font-size: 1rem;
    font-style: bold;
    margin-left: 1rem;
}

h2 {
    font-size: 0.75rem;
}

p {
    font-size: 0.5rem;
}

.icon-container {
    flex: 1;
    margin: 0 auto;
    display: flex;
    border-radius: 0.75rem;
    background-color: black;
    color: white;
    padding: 0;
    height: 2.7rem;
    max-width: 2.5rem;
}

[class^='fa fa-'] {
  display: flex;
  margin: 0 auto;
  margin-top: 0.75rem;
  font-size: 1rem;
}

.text-container {
    flex: 4;
    margin-left: 0.5rem;
    justify-content: center;
    margin-top: 0.4rem;
    line-height: 0.3rem;
}
</style>