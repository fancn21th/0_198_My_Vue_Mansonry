<template>
  <div ref="grid">
    <div class="grid-item height-5">1</div>
    <div class="grid-item height-10">2</div>
    <div class="grid-item height-20">3</div>
    <div class="grid-item height-30">4</div>
    <div class="grid-item height-40">5</div>
    <div class="grid-item height-30">6</div>
    <div class="grid-item height-20">7</div>
  </div>
</template>

<script>
import Masonry from 'masonry-layout'

export default {
  mounted() {
    const m = new Masonry( this.$refs.grid, {
      itemSelector: '.grid-item',
    });

    console.log(m)
  },
}
</script>

<style>
.grid-item { width: 25%; border: 1px dashed #ccc; display: flex; align-items: center; justify-content: center; }
.height-5 { height: 5rem }
.height-10 { height: 10rem }
.height-20 { height: 20rem }
.height-30 { height: 30rem }
.height-40 { height: 40rem }
</style>