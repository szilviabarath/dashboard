<template>
    <div class="wrapper">
    <h1>Recent emails</h1>
<table>
  <tbody>
    <tr v-for="item in items" :key="item.name">
      <td><img :src="item.image"></td>
      <td>{{ item.name }}</td>
      <td class="name">{{ item.subject }}</td>
      <td class="time">{{ item.time }}</td>
    </tr>
  </tbody>
</table>
</div>


</template>

<script>
export default {
name: 'EmailInbox',
    data() {
      return {
        items: [
          {
            image: "https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=464&q=80",
            name: "Hannah Morgan",
            subject: "Meeting scheduled",
            time: "1:24 PM"
          },
          {
            image: "https://images.unsplash.com/photo-1554727242-741c14fa561c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
            name: "Megan Clark",
            subject: "Update on marketing campaign",
            time: "12:32 PM"
          },
          {
            image: "https://images.unsplash.com/photo-1583195763986-0231686dcd43?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=876&q=80",
            name: "Brandon Williams",
            subject: "Designly 2.0 is about to launch",
            time: "Yesterday at 8:57 PM"
          },
          {
            image: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=464&q=80",
            name: "Reid Smith",
            subject: "My friend Julie loves Dappr!",
            time: "Yesterday at 8:49 PM"
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
  background-color: #d0e1e9 !important;
  padding: 2rem;
  width: 100%;
  margin-bottom: -50px;
}

table {
  border-spacing: 2rem;
  width: 100%;
}
td {
  white-space: nowrap;
  font-size: 0.75rem;
  height: 50px;
}

tr {
  margin-right: 5rem;
}

h1 {
  font-size: 1rem;
}

img {
  border-radius: 50%;
  height: 2rem;
  width: 2rem;
  object-fit: cover;
  object-position: top center;
}

.wrapper tbody > tr:nth-of-type(1) img {
  object-position: center center;
}
.name {
  text-align: justify;
}
.time {
  text-align: right;
  font-size: 0.5rem;
}


</style>