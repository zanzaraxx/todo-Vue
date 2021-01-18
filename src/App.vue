<template>
  <div id="app">
    <mainHeader />
    <container />
    <mainFooter />
  </div>
</template>

<script>
import mainHeader from './components/mainHeader.vue';
import container from './components/container.vue';
import mainFooter from './components/mainFooter.vue';


export default {
  name: 'app',

  components: {
    mainHeader,
    container,
    mainFooter
  }, 
};
</script>;