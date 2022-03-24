<template>
<div>
    <div v-text="title"></div>
    <div v-if="showName">
    <p>{{user.firstName}}</p>
    </div>
    <div v-else>
        <p>No puedo mostrar nada mi pez</p>
    </div>
    <hr>
    <ul>
        <li v-for="task in tasks">
        {{task.title}}
        </li>
    </ul>
</div>
</template>

<script>
export default {
   data(){
       return {
           title: "Hola CumJS",
           user: {
               firstName: "Julio",
               lastName: "Casas"
           },
           myHtml: "<h2>Hola vueuwu</h2>",
           showName: false,
           tasks: [
               {title: 'eat'},
               {title: 'dinner'},
               {title: 'lunch'}
           ]
       }
   }
}
</script>

<style media="screen">

</style>
