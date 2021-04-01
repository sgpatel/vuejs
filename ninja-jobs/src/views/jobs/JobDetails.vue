<template>
<div>
  <h1>Job Details Page</h1>
  <p>Job Id : {{ id }}</p>
</div>
</template>
<script>
export default {
  data() {
    return {
        id: this.$route.params.id
    };
  }
};
</script>