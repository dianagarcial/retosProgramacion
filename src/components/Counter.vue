<template>
    <div class="componente">
    <h1>{{ title}}</h1>
    <span>{{counterNumber}} * {{counterNumber}}={{getMultiplication}}</span><br/>
    <button @click="increase"> +1</button>
    <button @click="decrease"> -1</button>
</div>
</template>

<script>
    export default{
        props:{
            title: String,
            start:{
                type:Number,
                default: 10,
                required: false,
                validator:(value)=>{
                    return value >= 0
                }
            }
        },
        name:'Counter',
        data(){
            return{
                counterNumber :5
            }
        },
        methods:{
            increase(){
                console.log('calling increase');
                this.counterNumber ++;
            },
            decrease(){
                console.log('calling decrease');
                this.counterNumber --;
                
            }
        },
        computed: {
            getMultiplication(){
                console.log('calling method');
                return this.counterNumber * this.counterNumber
            }
        }
    }

</script>

<style>

    button{
        background-color: bisque;
    }

</style>