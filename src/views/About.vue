<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2>{{ haha }}</h2>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  props: ["items"],
  data: () => ({
    drawer: null,
    haha: this.$props["results"],
  }),

  //   async created()
  //   {

  //  console.log(res.data);
  //  return res.data;
  //   }
};
</script>
