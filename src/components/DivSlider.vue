<template>
    <div>
      <div class="container p-0">
        <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 16 16" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 01.708 0l6 6a.5.5 0 010 .708l-6 6a.5.5 0 01-.708-.708L10.293 8 4.646 2.354a.5.5 0 010-.708z" clip-rule="evenodd"></path></svg>
        <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 16 16" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 010 .708L5.707 8l5.647 5.646a.5.5 0 01-.708.708l-6-6a.5.5 0 010-.708l6-6a.5.5 0 01.708 0z" clip-rule="evenodd"></path></svg>
        <div class="wrap">
          <div class="card-container" v-for="(item, index) in items" :key="index">
            <div class="card p-2">
              <div class="card-header d-flex justify-content-between">
                <i :class="'fa fa-' + item.icon"></i>
                <i class="fa fa-ellipsis-v ellipsis"></i>
              </div>
              <div class="card-body p-2">
                <h2>{{ item.balance }}</h2>
                <p>{{ item.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>

  <script>
  export default {
    name: "DivSlider",
    data() {
      return {
        items: [
          {
            icon: "money",
            balance: "$143,624",
            description: "Your bank balance"
          },
          {
            icon: "pie-chart",
            balance: "12",
            description: "Unauthorized transactions"
          },
          {
            icon: "camera",
            balance: "7",
            description: "Employees working today"
          },
          {
            icon: "credit-card",
            balance: "$3,287.49",
            description: "This week's card spending"
          }
        ]
      };
    }
  }
  </script>

<style scoped>

.wrap {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(4, calc(96% / 4));
  justify-content: space-between;
}

.container {
  margin-top: 3rem;
  width: 111%;
}


.col-3 {
  width: 12.5rem;
  height: 12.5rem;
}
.card {
    border-radius: 1.25rem;
    border: none;
    background-color: #d0e1e9 !important;
    height: 10rem;

}

.card-header {
    background-color: #d0e1e9 !important;
    border: none !important;
    border-radius: 50% !important;
}

svg {
  float: right;
  margin-bottom: 10px;
  margin-right: 10px;
  padding-right: 2px;
}

.ellipsis {
display: flex;
  align-items: center;
  justify-content: center;
  height: 24px;
  width: 24px;
}
.ellipsis:hover {
  background-color: black;
  border-radius: 50%;
  color: white;
  align-items: center;
  justify-content: center;
  padding-left: 10px;
  margin-left: -10px;
  transition: color 0.2s ease-in-out;

}

[class^='fa fa-']:not(.fa-ellipsis-v) {
  font-size: 2rem;
  padding: 0.5rem;
}
[class^='fa fa-']::before {
  margin-left: -10px;
}

.fa-camera::before, .fa-money::before {
  margin-left: -13px;
}
.fa-pie-chart::before {
  margin-left: -15px;
}
h2 {
  font-size: 1rem;
  font-weight: bold;
  margin-left: 0.5rem;
}

p {
  margin-left: 0.5rem;
  font-size: 0.75rem;
  width: 6rem;
}

</style>