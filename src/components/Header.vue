<template>
  <div class="row mb-5 mt-5">
    <div class="col-sm">
      <p>Quote Added</p>
      <div class="progress" style="height: 20px;">
        <div class="progress-bar text-center" role="progressbar" style="width: 25%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" :style="{width:(quoteCount / maxQuote) * 100 + '%'}">
          {{ quoteCount }} / {{ maxQuote }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
      props : ['quoteCount', 'maxQuote']
    }
</script>

<style scoped>

</style>
