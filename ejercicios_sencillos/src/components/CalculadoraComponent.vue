<template>
<router-link to="/">Home</router-link>
<h1>Calculadora</h1>
  <div class="hello">
      <button @click="renderizarGUI">Calculadora</button>
  </div>
  

</template>

<script>
export default {
  name: "CalculadoraComponent",
  props: {
    msg: String,
  },
  methods: {
    renderizarGUI(){
    
    //Div Calculadora
    const divCalculadora= document.createElement("div")
    divCalculadora.setAttribute("id", "calculadora");
    divCalculadora.setAttribute("class", "text-center")
    divCalculadora.setAttribute("style", "width:50%; margin:0 auto;")
    document.body.appendChild(divCalculadora);
    
    //Div Pantalla
    const divPantalla= document.createElement("div")
    divPantalla.setAttribute("id", "divPantalla");
    divCalculadora.appendChild(divPantalla);

    //Pantalla
    const pantalla= document.createElement("input")
    pantalla.setAttribute("id", "pantalla");
    pantalla.setAttribute("type", "text");
    pantalla.setAttribute("value", "0");
    pantalla.setAttribute("disabled", "true");
    pantalla.setAttribute("class", "form-control text-right")
    //Agregar pantalla en la divPantalla
    divPantalla.appendChild(pantalla);

    //Div Botones
    const divBotones= document.createElement("div")
    divBotones.setAttribute("id", "botones");
    divCalculadora.appendChild(divBotones);



    }
    

  },
  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

h4 {
  font: 1.5em/1.5em "handwriting", cursive, sans-serif;
}

h6 {
  margin-bottom: 3px;
}

h3,
h6,
input {
  font: 1em/1.5em "handwriting", cursive, sans-serif;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

input {
  margin: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

form {
  display: flex;
}

section {
  width: 50%;
  display: inline-block;
}

.columna-izquierda {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
}

.columna-derecha {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: left;
}

input,
h6 {
  text-align: left;
}
</style>
