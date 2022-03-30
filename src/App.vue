<template>
  <div>Hello {{ value }}
    <div class="col-sm12">
      <label>足し算:</label>
      <input type="number" v-model.number="input1_1"> + 
      <input type="number" v-model.number="input1_2"> = 
      <span id='addval'>{{ add1 }}</span>
    </div>
    <div class="col-sm12">
      <label>割り算:</label>
      <input type="number" v-model.number="input2_1"> + 
      <input type="number" v-model.number="input2_2"> = 
      <span id='divval'>{{ div1 }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      input1_1:0,
      input1_2:0,
      input2_1:0,
      input2_2:0,
      value: "World",
    }
  },
  computed: {
    add1: function() {return this.input1_1 + this.input1_2},
    div1: function() {return this.input2_1 / this.input2_2}
  },
};
</script>
