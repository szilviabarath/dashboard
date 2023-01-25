<template>
    <div class="p-4 mt-0 container" v-for="item in items" :key="item.title">
      <h2> {{ item.title }}</h2>
      <div class="data-container d-flex justify-content-between">
        <h1 class="mr-2 display-2">{{ item.data }}</h1>
        <p :class="percentageColor(item.percentage)">{{ item.percentage }}</p>
      </div>
    </div>
</template>


<script>
export default {
  name: 'BoxStack',
  methods: {
  percentageColor(percentage) {
    console.log(percentage)
    if (parseFloat(percentage) < 10) {
      return "red-percentage";
    } else {
      return "green-percentage";
    }
  }
},
data() {
      return {
        items: [
          {
            title: "New clients",
            data: 54,
            percentage: "+18.7%"
          },
          {
            title: "Invoices overdue",
            data: 6,
            percentage: "+2.7%"
          }
        ]
      };

    }
  }
</script>


  <style scoped>
.container {
  border-radius: 1.25rem;
  border: none;
  background-color: #d0e1e9 !important;
  max-width: 12.5rem;
  height: 8rem;
  flex-wrap: nowrap;
  margin-top: 1rem;
}

.data-container{
  max-width: 100%;
  align-items: center;
  justify-content: center;
  display: flex;
}

h1 {
  font-size: 2rem;
  font-weight: bold;
  align-items: flex-start;
  justify-content: flex-start;
  flex: 1;
}

h2 {
  font-size: 0.75rem;
  text-align: justify;
  font-weight: bold;
}

p {
  font-size: 0.75rem;
  margin: 0;
  flex: 1;
  border-radius: 3px;
  text-align: center;
}

.green-percentage {
  background-color: #b9d6cb;
  color: #72aa72;
}

.red-percentage {
  background-color: #d8bfcc;
  color: #b35f71;
}
</style>
