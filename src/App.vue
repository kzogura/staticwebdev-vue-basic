<template>
  <div>Hello {{ value }}</div>
  <div class="col-sm12">
    <label>足し算:</label>
    <input type="number" v-model.number="input1_1"> + 
    <input type="number" v-model.number="input1_2"> = 
    <span>{{ add1 }}</span>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    input1_1:0,
    input1_2:0,
    return {
      value: "World"
    };
  },
  computed: {
    add1: function() {return this.input1_1 + this.input1_2}
  },
};
</script>
