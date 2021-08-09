<template>
  <div>
    <ul>
      <li v-for="index in msg" :key="index">hello</li>
    </ul>
    <button @click="sendname">Send Name</button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
@Component({
  props: {
    msg: { default: 0 },
  },
})
export default class newcomp extends Vue {
  sendname() {
    this.$emit("nameupdate", "Abdullah Iqbal");
  }
}
</script>
