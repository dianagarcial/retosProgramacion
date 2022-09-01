<template>
  <div class="body">
   
   <HelloWorld></HelloWorld>
   
   <Counter title="Counter1"></Counter>
   <Counter :start="15"></Counter>
   
   <IfelseComponent></IfelseComponent>
   <Show></Show>
   <Indecision></Indecision>
   <Fetch></Fetch>
   
  </div>
 
 </template>
 
 <script>
 
   
 import HelloWorld from './components/HelloWorld.vue';
 import Counter from './components/Counter.vue';
 import IfelseComponent from './components/ifelsecomponent.vue';
 import Show from './components/show.vue';
 import Indecision from './components/indecision.vue';
 import Fetch from './components/fetchApi.vue';
 export default{
     name:'App',
     components:{
     HelloWorld,
     Counter,
     IfelseComponent,
     Show,
     Indecision,
     Fetch
 }
   }
 </script>
 <style>
 
 .componente{
   margin: 2%;
 }
 .columna{
   display: flex;
   flex-direction: column;
 }
 .body{
   margin:2em
 }
 
 input{
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 300;
 font-size: 0.8em;
 line-height: 1.5em;
 text-align: left;
 text-indent: 5px;
 background-color: antiquewhite;
 border-radius: 1em;
 outline: none;
 border: 0.1em solid #B88C94;
 padding: 5px;
 
 }
 
 button{
   background-color: #B88C94;
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 200;
 font-size: 1em;
 line-height: 1.5em;
 text-align: center;
 text-indent: 5px;
 color: antiquewhite;
 width: 50px;
 align-content: center;
 border: 0.1em solid #B88C94;
 border-radius: 0.2em;
 margin-left: 2% ;
 
 
 }
 h1{
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 700;
 font-size: 1em;
 line-height: 1.5em;
 text-align: left;
 text-indent: 5px;
 }
 h2{
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 200;
 font-size: 1em;
 line-height: 1.5em;
 text-align: left;
 text-indent: 5px;
 }
 
 h3{
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 400;
 font-size: 0.8em;
 line-height: 1.5em;
 text-align: right;
 text-indent: 5px;
 margin:2em
 }
 span{
   font-family: 'Montserrat';
 font-style: normal;
 font-weight: 500;
 font-size: 1em;
 line-height: 1.5em;
 text-align: left;
 text-indent: 5px;
 }
 
 
 </style>
 
 
 
 