<template>
  <header>
    <div class="title">
      {{title}}
    </div>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
        <li><a href=""></a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {

  data() {
    return {
      title:'header title'
    };
  }
};
</script>

<style lang="scss" scoped>
header{
  background: #333;
  color:#fff;
  padding:15px;
  a{
    color:#fff;
  }
}
</style>
