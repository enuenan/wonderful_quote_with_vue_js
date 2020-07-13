<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="card card-default mt-2">
      <div class="card-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props : ['quote']
  }
</script>

<style scoped>
  .card-body{
    font-family: 'Lobster Two', cursive;
    font-size: 25px;
    color: #1a6482;
  }

  .quote{
    cursor: pointer;
  }

  .quote:hover{
    background-color: #ffe2e2;
  }
</style>
