<template>
  <div class="footer">
      <div class="p-toolbar-group-left">
        <span>@fab1an._sb3 © 2024</span>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  background-color: rgba(32, 68, 121, 0.99);
  text-align: center;
  padding: 10px 0;
  box-shadow: 0 -2px 5px rgb(246, 246, 246);
}
.p-toolbar-group-left {
  color: white;
}
</style>