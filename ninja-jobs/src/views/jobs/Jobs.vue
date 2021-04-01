<template>
<h1>New Jobs</h1>
    <div v-for="job in jobs" :key="job.id">
       <router-link :to="{name:'JobDetails', params:{id: job.id}}"><h1>{{job.title}}</h1></router-link>
    </div>
 <router-view/>
</template>
<script>
export default {
    data(){
        return{
            jobs:[
                {title:'Java developer',id : 1, details: 'java' },
                {title:'fornt end Developer', id:2, details:'Html Css'},
                {title:'Dotnet Developer',id:3, details:' C shorp'}

            ]
        }
    }
}
</script>
<style >

</style>