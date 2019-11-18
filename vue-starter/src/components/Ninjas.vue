<template>
  <div>
    <h1>Hello Ninjas.vue</h1>
    <ul>
      <li v-for="ninja in ninjas" v-on:click="ninja.show=!ninja.show">
        <h2>
          {{ninja.name}}
        </h2>
        <h3 v-show="ninja.show">
          {{ninja.speciality}}
        </h3>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ninja",
  data() {
    return {
      ninjas:[
       {name: 'Ryu',speciality:'Vue Compontents', show:false},
       {name: 'Crystal',speciality:'HTML Wizardry', show:false},
       {name: 'Hitoshi',speciality:'Click Events', show:false},
       {name: 'Tango',speciality:'Conditions', show:false},
       {name: 'Kami',speciality:'Webpack', show:false},
       {name: 'Yoshi',speciality:'Data Diggin', show:false},
        ]
    };
  }
};
</script>

<style lang="scss">
</style>
