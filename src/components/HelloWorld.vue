<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div v-for="i in 100" :key="'wddwdw'+i" class="test">
      {{i}}
      <square/>
    </div>
  </div>
</template>

<script>
import square from './Square.vue';

export default {
  name: 'HelloWorld',
  components: { square },
  props: {
    msg: String,
  },
  methods: {

  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
