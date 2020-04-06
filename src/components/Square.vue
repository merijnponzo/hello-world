<template>
  <div class="hewllo">
    <a @click="getB()">good bounding values</a>
    <router-link @click.native="getB()" to="/about">
    wrong bounding values
    </router-link>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  methods: {
    getB() {
      const ref = this.$el;
      const bounds = ref.getBoundingClientRect();
      /* eslint-disable no-console */
      console.log(bounds);
      /* eslint-enable no-console */
      this.$router.push({ path: 'about' })
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a{
  color:white;
  display:block;
  border:2px solid white;
  padding:5px;
  margin:5px;
  cursor: pointer;
}
.hewllo{
  display:flex;
  margin-bottom:2px;
  margin:0 auto;
  flex-direction: column;
  align-items: center;
  width:48%;
  background:black;
  height:400px;
}
</style>
