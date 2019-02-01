<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
    <p>{{theJsonData}}</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

import theJson from '@/assets/hi.json';

export default Vue.extend({
  name: 'home',
  components: {
    HelloWorld,
  },
  async mounted() {
    console.log('HOII');
    console.log(theJson);
    this.theJsonData = JSON.stringify(theJson.abi);
  },
  data() {
    return {
      theJsonData: 'nojsondataloaded',
    };
  },
});
</script>
