<template>
  <div id="app">
    <dv-loading>Loading...</dv-loading>
    <div class="dv">
      <dv-border-box-1></dv-border-box-1>
    </div>
    <dv-border-box-8></dv-border-box-8>
    <div class="dv">
      <dv-border-box-12></dv-border-box-12>
    </div>
    <div class="dv">
      <dv-border-box-13></dv-border-box-13>
    </div>
    <div class="dv">
      <dv-decoration-1 :color="['red', 'green']" />
    </div>
    <div class="dv">
      <dv-decoration-2/>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style>
#app {
  width: 90vw;
}
#app .dv-border-box-8 {
  width: 300px;
  height: 300px;
  margin: 20px;
}
.dv .dv-border-box-1,
.dv .dv-border-box-12,
.dv .dv-border-box-13,
.dv .dv-decoration-2 {
  width: 300px;
  height: 300px;
  margin: 20px;
}
</style>
