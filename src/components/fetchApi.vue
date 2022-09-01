<template>
  
  <div class="componente">
    
    <h1>FETCH API</h1>
    <div id="columna">
      <input type="text" v-model="pregunta"  />
    </div>
    
    <img id="imagen"/>
    <span style="display:none;">{{apim()}}</span>
    
    

  </div>

</template>

<script>
export default {
  name: 'Fetch-API',

  data() {
    return {

      pregunta: ''
      

    }


  },
  
  methods: {
    async apim() {
      
        const api = await fetch("https://yesno.Wtf/api")
        
        const data = await api.json();
        const imagen=data.image;
        if(this.pregunta.includes('?')){
          document.getElementById("imagen").setAttribute('src', imagen);
        }else{
          document.getElementById("imagen").setAttribute('src', '');
        }
        console.log(data)
        return ''
        
        

    }

  }

}
</script>

