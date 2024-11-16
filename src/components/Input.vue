<template>
  <input
    type="number"
    @input="changeAmount($event.target.value)"
    placeholder="Enter Number"
    min="0"
  /><br >
  <button @click="convert()">Convert</button>
</template>

<script>
export default {
  props: {
    changeAmount: {
      type: Function,
      required: true,
    },
    convert: {
      type: Function,
      required: true,
    },
  },
};
</script>

<style scoped>
input {
  font-size: 1.2em;
  width: 400px;
  position: relative;
  top: -20px;
  border-radius: 3px;
  border: 1px solid transparent;
  padding: 10px 15px;
  background: #fafafa;
  outline: none;
}

button {
    position: relative;
    top: 20px;
    padding: 10px 25px;
    color: #fafafa;
    text-transform: uppercase;
    cursor: pointer;
    background: #1a032d;
    border: 0;
    border-radius: 3px;
}

</style>
