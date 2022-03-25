<template>
<div class="test">
    {{msg}}
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
    },
        computed: {
            fullName(){
                return `${this.user.firstName} ${this.user.lastName}`
            }
        },
        props: {
            msg: {
                type: String,
                default: 'Mensaje por defecto'
            }
        } 
}
</script>

<style media="screen">
    .test {
        background-color: blue;
    }

</style>
