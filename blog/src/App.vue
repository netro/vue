<template>
  <div>
    <add-blog></add-blog>
  </div>
</template>

<script>
import Blog from "./components/addBlog.vue";

export default {
  components: {
    'add-blog': Blog
  },
  data() {
    return {};
  },
  methods: {}
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
