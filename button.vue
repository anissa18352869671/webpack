<template>
  <button @click="handleClick" :style="styles">
    <slot></slot>
  </button>
</template>
<script>
export default {
  props: {
    color: {
      type: String,
      default: "#00cc66"
    }
  },
  data() {
    return {
      myColor: this.color
    };
  },
  computed: {
    styles() {
      return {
        background: this.myColor
      };
    }
  },
  methods: {
    handleClick(e) {
      this.myColor = "red";
      this.$emit("click", e);
      //   console.log(this);
    }
  }
};
</script>
<style scoped>
button {
  border: 0;
  outline: none;
  color: #fff;
  padding: 4px 8px;
}
button:active {
  position: relative;
  top: 1px;
  left: 1px;
}
</style>