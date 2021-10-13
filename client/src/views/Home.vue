<template>

  <BasicLayouts>
    
    <h1 class ="tituloPrincipal">Bienvenidos a Ristorante Carpincho</h1>
<div id="about" class="about-main pad-top-100 pad-bottom-100">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                    <div class="wow fadeIn" data-wow-duration="1s" data-wow-delay="0.1s">
                    </div>
                </div>
            </div>
         </div>
 </div>               
 <!--*---NOSOTROS ------------------------------------------------------------------->                       
   <div>                     
    <h2 class="block-title">Nosotros </h2>
		</div>
       <div> 
      <div class="texto">
                 <p> Conece sobre nuestros objetivos y compromisos. </p>
 						</div>
      <br><br><br>
            <h3 class="subt">Misión</h3>
       </div>
          <div class="texto">
                 <p> Reconocer y cumplir con las expectativas gastronómicas de nuestros clientes, en cocina oriental, ofrecer servicios, platos y atenciones  de calidad que permitan crear huella en nuestros colaboradores, clientes y el entorno. </p>
 						</div>
        <div>
          <br> 
             <h3 class="subt">Visión</h3>
        </div>
             <div class="texto">
                        <p> A Ser el Mejor Restaurante a nivel Regional y nacional de cocina oriental Gourmet, reconocido y preferido por nuestros selectos clientes, como un sólido grupo gastronómico profesional para 2025. </p>
            </div>
<br><br><br><br><br><br>
 <!--*---Carta Digital ------------------------------------------------------------------->                       
   <div>                     
    <h2 class="block-title">Nuestro carta digital </h2>
		</div>  


    <br><br><br><br>      
                <!-- end col -->
                <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                    <div class="wow fadeIn" data-wow-duration="1s" data-wow-delay="0.1s">
                        <div class="about-images">
                            <img class="about-main" src="../assets/about-main.jpg" alt="About Main Image">

                        </div>
                    </div>
                </div>
                <!-- end col -->
         <br><br><br><br> 
          <div class="texto">
                 <p> Ven, descarga nuestra carta y come en nuestro restaurante </p>
   <div>
                            <img class="about-main" src="../assets/Men.jpg" alt="Menu">
                        </div>

 						</div>
            <!-- end row -->
<br><br><br>
        <!-- end container -->
<div>
   <!--*---Compra en linea ------------------------------------------------------------------->                          
    <h2 class="block-title">Nuestros productos en domicilio </h2>
		</div>
    <br><br>
    <div class="texto">
                        <p> Selecciona el prodcuto que mas te guste y disfruta de la especialidad de la casa </p>
            </div>
    <br><br><br><br>
    <div class="ui grid">
      <div
        class="sixten wide mobile eight wide tablet four wide computer column"
        v-for="product in products"
        :key="product.id"
      >
        <Product :product="product" />
      </div>
    </div>
<br><br><br><br>
    <!-- Add icon library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<!-- Add font awesome icons -->
<a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a>

  </BasicLayouts>








</template>

<script>
import { ref, onMounted } from 'vue';
import BasicLayouts from '../layouts/BasicLayouts.vue';
import { getProducts } from '../api/products';
import Product from '../components/Product.vue';
export default {
  name: 'Home',
  components: {
    BasicLayouts,
    Product,
  },

  setup() {
    let products = ref(null);

    onMounted(async () => {
      const response = await getProducts(20);
      products.value = response;
    });
    return {
      products,
    };
  },
};

</script>



<style lanf = "scss" scoped>


.tituloPrincipal{
  color: black;
  text-align: center;
  font-weight: 10px;
  font-style: normal;
  font-family: "Flaticon" ;
  background-color: rgb(241, 31, 3);
}
.mision {
  color: white;
  text-align: center;
}

.subt{
  color: white;
  font-family: 'nautilus_pompiliusregular';
  text-align: center;
  font-size: 70px;
  }


.texto{
    color: white;
  text-align: center;
  font-weight: 520px;
  font-size: 30px;
}


.uno{
  color: white;
  text-align: center;
  font-weight: 90px;
}
.dos{
  color: white;
  text-align: center;
  font-weight: 90px;
}

.about-main{
	background:#000000;
}
.pad-top-100{
    padding-top: 0px;
}
.pad-bottom-100{
	padding-bottom: 0px;
}

.pad-top-70{
	padding-top: 70px;
}
.pad-bottom-70{
	padding-bottom: 70px;
}

.block-title{
	font-size:150px;
	font-family: 'nautilus_pompiliusregular';
	font-weight: bold;
  color: white;
  text-align: center;
}

.about-images {
    text-align: center;
    position: relative;
}

.about-main h3{
	font-family: 'Roboto', sans-serif;
    font-weight: 600;
	font-size:20px;
}

.left-btn{
	padding-top:10px;
}


.about-images img {
    border: 10px solid #f1f1f1;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    -webkit-border-radius: 999px;
    -moz-border-radius: 999px;
    border-radius: 999px;
}

.about-images img {
    border: 10px solid #f1f1f1;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    -webkit-border-radius: 999px;
    -moz-border-radius: 999px;
    border-radius: 999px;
	max-width: 100%;
}

.about-inset {
    position: absolute;
    top: 0;
    right: 0;
}


/* Style all font awesome icons */
.fa {
  padding: 20px;
  font-size: 30px;
  width: 50px;
  text-decoration: none;
  position: center;
  text-align: center;
  align-content: center;
  justify-content: center;
  margin:auto;
}

/* Add a hover effect if you want */
.fa:hover {
  opacity: 0.7;
}

/* Set a specific color for each brand */

/* Facebook */
.fa-facebook {
  background: #3B5998;
  color: white;
  
}

/* Twitter */
.fa-twitter {
  background: #55ACEE;
  color: white;
}


/*------------------------------------------------------------------
    SKELETON
-------------------------------------------------------------------*/
@font-face {
    font-family: 'nautilus_pompiliusregular';
    src: url('../fonts/nautilus-webfont.woff2') format('woff2'),
         url('../fonts/nautilus-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}




</style>