<template>
  <div class="row">
    <div class="col-sm-8 mx-auto col-xs-12 col-md-6 ">
      <form action="">
        <div class="form-group">
          <label>Quote</label>
          <textarea class="form-control" rows="3" v-model="quote"></textarea>
        </div>
        <div class="form-group">
          <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
    export default {
      data : function () {
        return {
          quote : ''
        };
      },
      methods : {
        createNew () {
          this.$emit('addedQuote', this.quote);
          this.quote = '';
        }
      }
    }
</script>

<style scoped>

</style>
