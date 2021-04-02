<template>
<div v-if="job">
  <h1>Job Details Page</h1>
  <h3>{{job.title}}</h3>
  <p>Job Id : {{ id }}</p>
  <p>{{job.details}}</p>
</div>
<div v-else>
  job details data is loading ....
</div>
</template>
<script>
export default {
  props:['id'],
  data() {
    return {
         job : null
    }
  },
  mounted(){
    fetch('http://localhost:3000/jobs/'+this.id)
        .then((res)=>res.json())
        .then(data=>this.job =data)
        .catch(err=>console.log(err))
  }
};
</script>