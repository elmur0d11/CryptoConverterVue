<template>
  <ul>
    <li @click="selectItem('BTC')" :class="current == 'BTC' ? 'active' : ''">
      Bitcoin
    </li>
    <li @click="selectItem('ETH')" :class="current == 'BTC' ? 'active' : ''">
      ETH
    </li>
    <li @click="selectItem('USDT')" :class="current == 'BTC' ? 'active' : ''">
      USDT
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    setCrypto: {
      type: Function,
      required: true,
    },
  },
  data() {
    return {
      current: "",
    };
  },
  methods: {
    selectItem(val) {
      this.setCrypto(val);
      this.current = val;
    },
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  width: 200px;
  padding: 0;
  border-radius: 10px;
  border: 1px solid transparent;
}

li {
  display: block;
  background-color: #1a032d;
  color: #fff;
  padding: 20px 0;
}

li:hover,
li:active {
  background-color: #24043e;
  cursor: pointer;
}
</style>
