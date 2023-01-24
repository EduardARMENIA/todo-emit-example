<template>
  <div class="form">
    <form @submit.prevent>
      <input type="text" v-model="name" placeholder="name" />
      <input type="text" v-model="email" placeholder="Email" />
      <button type="submit" @click="submitData">Submit</button>
    </form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    submitData(e) {
      this.$emit("passData", { name: this.name, emial: this.email });
    },
  },
};
</script>