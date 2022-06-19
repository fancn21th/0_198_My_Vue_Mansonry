<template>
  <div ref="grid">
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
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
.grid-item { width: 25%; min-height: 100px; border: 1px dashed #ccc }

</style>