<template>
  <div>
    <DeliHeader heading="Deli Store" />
    <DeliMain :items="items" />
  </div>
</template>

<script>
import DeliHeader from './components/DeliHeader.vue';
import DeliMain from './components/DeliMain.vue';

export default {
  name: 'App',
  components: {
    DeliHeader, 
    DeliMain,
  },
  data() {
    return {
      items: []
    };
  },
  methods: {
    async fetchDeliDetails() {
      try {
        const res = await fetch("https://delistore.onrender.com/api");
        const data = await res.json();
        console.log(data);
        return data.Deli;
      } catch (error) {
        console.error("Error fetching items:", error);
        return [];
      }
    },
  },
  async created() {
    this.items = await this.fetchDeliDetails();
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}

.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div {
  margin-bottom: 0.5em;
}
</style>
