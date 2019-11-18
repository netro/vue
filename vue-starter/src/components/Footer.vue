<template>
  <footer>
    <div>
      All right reserved to {{company}} {{title}}@
    </div>

  </footer>
</template>

<script>
export default {
  data() {
    return {
      company: 'NETRO SOLUTIONS',
      title: 'hello world'
    };
  },
  methods:{
    changeTitle: function () {
      this.$emit('changeTitle','NEW TITLE');
    }
  }
};
</script>

<style lang="scss" scoped>
footer{
  background: #333;
  color:#fff;
  padding:15px;
  a{
    color:#fff;
  }
}
</style>
