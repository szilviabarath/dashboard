<template>
  <div class="container-fluid position-relative justify-content-center">
    <div class="d-flex title-text">
    <h1 class="welcome-text">Good morning, James!</h1>
    <AccountInfo></AccountInfo>
  </div>
    <div class="row align-items-start">
      <div class="col-1">
        <NavBar></NavBar>
      </div>
      <div class="col-7 mt-5 pt-0 px-0 ml-0 slider-container d-flex flex-wrap">
        <DivSlider></DivSlider>
        <div class="col-4 pl-0 box-container spacer">
        <BoxStack class="mt-0"></BoxStack>
      </div>
        <LineChart class="col-8 spacer"></LineChart>
        <div class="w-100 inbox-container">
            <div class="col-12 p-0 pr-0">
            <EmailInbox></EmailInbox>
          </div>
        </div>
      </div>
      <div class="col-4">
        <FormationStatus class="p-4"></FormationStatus>
        <ToDoList class="mt-3"></ToDoList>
              <CalendarEvent></CalendarEvent>
          </div>
    </div>
  </div>


</template>


<script>
import NavBar from './components/NavBar.vue'
import AccountInfo from './components/AccountInfo.vue'
import DivSlider from './components/DivSlider.vue'
import FormationStatus from './components/FormationStatus.vue'
import BoxStack from './components/BoxStack.vue'
import LineChart from './components/LineChart.vue'
import ToDoList from './components/ToDoList.vue'
import CalendarEvent from './components/CalendarEvent.vue'
import EmailInbox from './components/EmailInbox.vue'



export default {
  name: 'App',
  components: {
    NavBar,
    AccountInfo,
    DivSlider,
    FormationStatus,
    BoxStack,
    LineChart,
    ToDoList,
    CalendarEvent,
    EmailInbox
  },


}
</script>

<style>
#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #ecf4fa;
  padding: 1.25rem;
  border-radius: 1.9rem;
  margin: 1.25rem;
  height: 48.125rem;
  padding-top: 1.875rem;
}

.container-fluid {
  width: 100%;
  height: 43.75rem;
  display: flex;
  flex-direction: column;
  padding: 1.25rem;
}

.spacer {
  margin-top: 2rem !important;
}

.box-container > div:nth-child(2) {
  margin-top: 1rem !important;
}

.inbox-container {
  position: absolute;
  bottom: -9.375rem;
}

.slider-container {
  position: relative;
  padding-bottom: 7.5rem;
  padding-top: 15.625rem !important;
}

.welcome-text {
  text-align: left;
  flex: 1;
  margin-bottom: 2rem;
  font-size: 1.75rem;
  margin-top: -1rem;
  font-weight: bold;
}

.title-text {
  position: absolute;
  top: 0.3rem;
  right: 10px;
  width: calc(100% - 8.3% - 20px);
}

accountInfo {
  flex: 1;
}
</style>
