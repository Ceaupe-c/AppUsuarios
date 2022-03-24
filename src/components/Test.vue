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
        <li v-for="task in tasks" :key="task">
        {{task.title}}
        </li>
    </ul>
    <hr>
    <div>
        <input type="text" v-model="user.firstName">
        <button type="button" name="button" v-on:click="saludar(user.firstName)">
            CLICK ME
        </button>
        <input type="text" v-on:keyup.enter="typedEnter">
    </div>
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
   },
   methods: {
       saludar(name){
           alert(`hellowo ${name}`);
       },
       typedEnter(){
           console.log("Dio un enter");
       }
   }
}
</script>

<style media="screen">

</style>
