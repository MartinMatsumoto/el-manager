<template>
</template>

<script>
  export default {
    name: 'text-utils',
    data() {
      return {}
    },
    authEmpty: function (text, errorCall, successCall) {
      if (text === undefined || text === null || text === '') {
        if (errorCall) {
          errorCall();
        }
        return false;
      }
      if (successCall) {
        successCall();
      }
      return true;
    }
  }
</script>

<style>
</style>
