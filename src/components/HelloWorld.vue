<template>
  <div class="hello">
    {{ count }}
    <button @click="decrement">-</button>
    <button @click="increment">+</button>
    <div>
      <p @click="hello">HELLO</p>
    </div>
    <newcomp :msg="count" />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import newcomp from "./newcomp.vue";
@Component({
  components: {
    newcomp,
  },
})
export default class HelloWorld extends Vue {
  count = 6;
  increment() {
    return this.count++;
  }
  decrement() {
    return this.count--;
  }
  hello() {
    alert("Hello to Class component \n Counter = " + this.count);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
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
button {
  padding: 3px;
  margin: 5px;
}
</style>
