<template>
  <div>
    <div>HELLO {{name}}</div>
    <div>{{data}}</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Anissa today",
      data: "啊飒飒!"
    };
  }
};
</script>
<style scoped>
div {
  color: #f60;
  font-size: 24px;
}
</style>
