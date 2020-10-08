<template>
  <nav :style="{ background: background || '#333' }">
      <ul :style="{ background: background || '#333' }">
          <li></li>
      </ul>

  </nav>
</template>

<script>
export default {
    props: ['navLinks','background']
}
</script>

<style scoped lang='scss'>

nav {
	height: 60px;
	width: 100%;
    ul {
        margin-block: 0;
    }
}
</style>