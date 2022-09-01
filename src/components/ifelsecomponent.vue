<template>
    <div class="componente">
    <input type="text" v-model="newMessage" @keypress.enter="addQuote()"/>
    {{newMessage}}
    <ul>
        <li v-for="(quote, index) in items" :key="quote">
            <span>{{index + 1}}. {{quote.mensaje}}</span>
            <span v-if="quote.author"> Por {{quote.author}}</span>
            <span v-else>No Author</span>

        </li>
    </ul>

    

    </div>
</template>
<script>
    export default{
        data(){
            return {
                newMessage:'',
                items: [
                    {mensaje:'Foo', author: 'Juan'},
                    {mensaje: 'Bar', author: 'Pedro'}
                ]
            }
        },
        methods:{
            addQuote(){
                this.items.unshift({
                    mensaje: this.newMessage,
                    author: 'Jlopez'
                })
            }
        }
    }
</script>