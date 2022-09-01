<template>
    <div class="componente">
    <img src="https://via.placeholder.com/250"/>
    <div class="bg-dark"></div>
    <div class="indecision-container">
        <input type="text" placeholder="Hazme una pregunta" v-model="question"/>
        <p>Recuerda finalizar con signo de interrogacion (?)</p>
    </div>

    <div>
        <h2>{{question}}</h2>
        <h1>SI, NO, ..... pensando</h1>
        </div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                question: ''
            }
        },
        watch:{
            question( value, oldValue){
                console.log(value, oldValue)
            }
        }
    }
</script>