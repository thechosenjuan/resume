<template>
  <div class="main-header">
    <h1>
      Juan Manuel Flores Barrera
      <span>Monterrey, México</span>
    </h1>
    <slot></slot>
  </div>
</template>

<style>
.main-header {
  display: grid;
  grid-template-columns: 1fr;
}
.main-header h1 {
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: space-between;
}
.main-header h1 span {
  font-size: 14.5px;
  vertical-align: middle;
}
</style>