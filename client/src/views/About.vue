<template>
    <BasicLayouts>
        <div>
            <h1 class="titulo1">¿Quiénes Somos?</h1>
  

<section class= "centrar">
   <div class="ui link cards">
  <div class="card">
    <div class="image">
      <img src="../assets/Luisa.jpg">
    </div>
    <div class="content">
      <div class="header">Luisa</div>
      <div class="meta">
        <a>Desarrollador</a>
      </div>
      <div class="description">
        Luisa es estudiante de Ingeniería Ambiental.
      </div>
    </div>
    <div class="extra content">
      <span class="right floated">
        Se unió desde 2020.
      </span>
      <span>
        <i class="user icon"></i>
        75 interacciones
      </span>
    </div>
  </div>
  <div class="card">
    <div class="image">
      <img src="../assets/richard.jpg">
    </div>
    <div class="content">
      <div class="header">Richard</div>
      <div class="meta">
        <span class="date">Scrum Master</span>
      </div>
      <div class="description">
        Richar es el líder del equipo, estudiante de Ingeniería Industrial.
      </div>
    </div>
    <div class="extra content">
      <span class="right floated">
        Se unió en 2020
      </span>
      <span>
        <i class="user icon"></i>
        35 interacciones
      </span>
    </div>
  </div>

 <div class="card">
    <div class="image">
      <img src="../assets/sergio.jpg">
    </div>
    <div class="content">
      <div class="header">Sergio</div>
      <div class="meta">
        <span class="date">Desarrollador</span>
      </div>
      <div class="description">
        Sergio es estudiante de maestría en Ingeniería Biomédica.
      </div>
    </div>
    <div class="extra content">
      <span class="right floated">
        Se unió desde 2020.
      </span>
      <span>
        <i class="user icon"></i>
        15 interacciones
      </span>
    </div>
  </div>



  
</div>


</section>
  <br>
<br>

<br>
<section class= "centrar2">
   <div class="ui link cards">
  <div class="card">
    <div class="image">
      <img src="../assets/camilo.jpg">
    </div>
    <div class="content">
      <div class="header">Camilo</div>
      <div class="meta">
        <a>Desarrollador</a>
      </div>
      <div class="description">
        Camilo es estudiante de maestría en Ingeniería Industrial.
      </div>
    </div>
    <div class="extra content">
      <span class="right floated">
        Se unió en 2020
      </span>
      <span>
        <i class="user icon"></i>
        75 interacciones
      </span>
    </div>
  </div>
  <div class="card">
    <div class="image">
      <img src="../assets/ingrid.jpg">
    </div>
    <div class="content">
      <div class="header">Ingrid</div>
      <div class="meta">
        <span class="date">Desarrollador</span>
      </div>
      <div class="description">
        Ingrid es estudiante de biología.
      </div>
    </div>
    <div class="extra content">
      <span class="right floated">
        Se unió en 2020
      </span>
      <span>
        <i class="user icon"></i>
        45 interacciones
      </span>
    </div>
  </div>

 



  
</div>

</section>



</div>
       
    </BasicLayouts>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';
import * as Yup from 'yup';
import BasicLayouts from '../layouts/BasicLayouts.vue';
export default {
  name: 'About',
  components: {
    BasicLayouts,
  },
        
};
</script>

<style lanf = "scss" scoped>


.titulo1{
  color: black;
  text-align: center;
  font-weight: 50px;
  font-style: normal;
  font-family: "nautilus_pompiliusregular" ;
  background-color: rgb(241, 31, 3);
}

.ui.card{
    align-content: center;
    justify-content: center;
    align-items: center;
    display: flex;
}

.izquierda{
    display: flex;
    justify-content: left;
    align-items: left;
}

.centrar {

  display: flex;
  justify-content: center;
  align-items: center;
  /* Fin del codigo para centrar*/
}

.centrar2 {

  display: flex;
  justify-content: center;
  align-items: center;
  /* Fin del codigo para centrar*/
}
.hijo {
  height: 10px;
  width: 10px;
  background: red;
}
</style>

