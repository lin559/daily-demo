<template>
  <div class="hello">
    <h1>撒发射点发生</h1>
    <h2>{{ msg }}</h2>
    <com1></com1>
  </div>
</template>

<script>
import com1 from "./HelloWorld1";
export default {
  name: "HelloWorld",
  data() {
    return {
      childMsg: "来自子元素的呐喊"
    };
  },
  mounted() {
    // console.log(this.$root);
    // this.$parent.test();
    // console.log(this.$parent.parentMsg);
  },
  props: {
    msg: String
  },
  inject: ["a"],
  components: {
    com1
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
