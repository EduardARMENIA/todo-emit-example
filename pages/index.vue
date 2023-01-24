<template>
  <div id="app">
    <Form @passData="GetData($event)" />
    <div>
      <h4>Data in Parent Component:</h4>
      {{ personInfo }}
    </div>
  </div>
</template>

<script>


export default {
  name: "App",
  data() {
    return {
      personInfo: "",
    };
  },

  methods: {
    GetData(data) {
      this.personInfo = data;
    },
  },
};
</script>