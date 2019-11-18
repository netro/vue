<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <h1>Hello App.vue</h1>
    <ninjas></ninjas>
    <app-footer v-bind:title="title" v-on:changeTitle="changeTitle($event)"></app-footer>

  </div>
</template>

<script>
import Header from './components/Head'
import Footer from './components/Footer'
import Ninjas from './components/Ninjas'
export default {
  components:{
    'app-header':Header,
    'app-footer':Footer,
    'ninjas':Ninjas,
  },
  data() {
    return {
      title:'This Is Main Title'
    };
  },
  methods:{
    updateTitle: function (updatedTitle) {
        this.title= updatedTitle;
    }
  }
};
</script>

<style lang="scss">
*{
  padding:0;
  margin:0;
  box-sizing: border-box;
}
</style>
