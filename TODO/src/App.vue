<script setup>



let total = 0
let listaDeProductos = [
  {
    name:'yuca',
    cantidad : 12+1,
    precio:1500,
    diasVencido :5

  },
  {
    name:'platano',
    cantidad : 10,
    precio:155500,
    diasVencido :1

    
  },
  {
    name:'arroz',
    cantidad : 0,
    precio:100,
    diasVencido :52

    
  }

]
function suma (cantidad,precio){
  total += cantidad * precio 
}




</script>

<template >
  <section class="padre ">
    <div class="contenedor">
  <div class="nombre"><h1>Rincon de la Sopa</h1></div>
  <section class="contenido">
    <div class="titulos">
      <div class="nameProducto"><h1>nombre producto</h1> </div>
      <div class="prof">
        <div class="cant"><h3>cantidad</h3></div>
        <div class="precio"><h3>precio</h3></div>
        <div class="diasVencer"><h3>dias vencer</h3></div>
      </div>
    </div>
   
    
  </section>
<span v-for="(objeto,index) in listaDeProductos " :key="index"   >   
  
  
  <h1 v-if="!(objeto.cantidad==0 || objeto.diasVencido==0 ) "> 
    
  
  
  <section class="contenido">
    <div class="todo">
      <div class="nameProduct"><h1>{{ objeto.name }}</h1> <h1 class="alerta" v-if="(objeto.diasVencido<3)"> esta por vencer </h1></div>
      <div class="pro">
        <div class="cant"><h3>{{ objeto.cantidad }}</h3></div>
        <div class="precio"><h3>{{ objeto.precio }}</h3></div>
        <div class="diasVencer"><h3>{{ objeto.diasVencido }}</h3></div>
      </div>
    </div>
   
    
  </section>
</h1>
{{ suma(objeto.cantidad,objeto.precio) }}
</span>
<h1 class="suma"> {{  total  }}</h1>
</div>

</section>

</template>

<style scoped>
.suma{
  display: flex;
justify-content: center;

}
.prof{
  background-color: #FFFFFF;
  display: flex;
  justify-content: space-evenly;
  width: 50%;
  margin-right: 10px;
  border-radius: 15px;

}

.nameProducto{
  
  display: flex;
  justify-content: center;
  width: 50%;


}
.titulos{
  display: flex;
  justify-content: space-around;
  padding: 10px 0;
}
.contenedor{
  background-color: #159A9C;
  border-radius: 15px;
  border: 2px white;
  max-width: 1000px;
  max-height: 1000px;
  margin: auto auto;
  padding: 15px;
}

.padre{
  background-color: #B4BEC9;
  padding: 15px;
}

.alerta{
  background-color: red;
  margin-left: 15px;
}

.todo{
  display: flex;
  justify-content: space-around;
  padding: 10px 0;
 
}
.nombre{
  margin-top: 15px;
  background-color: black;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  border-radius: 15px;
  color: white;
  
 
}
.contenido{
  background-color: #DEEFE7;
  margin: 0 auto;
  max-width: 1000px;
  margin: 0 auto;
  border-radius: 15px;
}
.nameProduct{
  margin-left: 15px;
  width: 50%;
  display: flex;
  

}
.pro{
  background-color: #FFFFFF;
  display: flex;
  justify-content: space-evenly;
  width: 50%;
  margin-right: 10px;
  border-radius: 15px;
  
}
.cant{
  background-color: #FFFFFF;
  padding: 0 15px;

}
.precio{
  background-color: #FFFFFF;
  padding: 0 15px;
  margin: 0 10px;
}
.diasVencer{
  background-color: red;
  padding: 0 15px;
 
}
.suma{
  color: white;
}

</style>
 
 