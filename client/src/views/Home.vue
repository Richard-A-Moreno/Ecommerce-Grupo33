<template>

  <BasicLayouts>
    
    <h1 class ="tituloPrincipal">Bienvenidos a Ristorante Carpincho</h1>

<div id="about" class="about-main pad-top-100 pad-bottom-100">
        <div class="container">
            <div class="row">
                <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                    <div class="wow fadeIn" data-wow-duration="1s" data-wow-delay="0.1s">
                        <h2 class="block-title"> Nosotros </h2>
						 <p></p>
                        <h3>Misión</h3>
                        <p> Reconocer y cumplir con las expectativas gastronómicas de nuestros clientes, en cocina oriental, ofrecer servicios, platos y atenciones  de calidad que permitan crear huella en nuestros colaboradores, clientes y el entorno. </p>
 						<h3>Visión</h3>
                        <p> A Ser el Mejor Restaurante a nivel Regional y nacional de cocina oriental Gourmet, reconocido y preferido por nuestros selectos clientes, como un sólido grupo gastronómico profesional para 2025. </p>

                    </div>
                </div>
                <!-- end col -->
                <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">
                    <div class="wow fadeIn" data-wow-duration="1s" data-wow-delay="0.1s">
                        <div class="about-images">
                            <img class="about-main" src="../assets/about-main.jpg" alt="About Main Image">
                            <img class="about-inset" src="../assets/about-inset.jpg" alt="About Inset Image">
                        </div>
                    </div>
                </div>
                <!-- end col -->
            </div>
            <!-- end row -->
        </div>
        <!-- end container -->
    </div>
    <div class="ui grid">
      <div
        class="sixten wide mobile eight wide tablet four wide computer column"
        v-for="product in products"
        :key="product.id"
      >
        <Product :product="product" />
      </div>
    </div>

    

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
  font-weight: 50px;
  font-style: normal;
  font-family: "Flaticon" ;
  background-color: rgb(241, 31, 3);
}
.mision {
  color: white;
  text-align: center;
}

.block-title{
  color: white;
  text-align: center;
  font-weight: 70px;
}

.uno{
  color: white;
  text-align: center;
  font-weight: 70px;
}
.dos{
  color: white;
  text-align: center;
  font-weight: 70px;
}

.texto{
    color: white;
  text-align: center;
  font-weight: 70px;
}

/*------------------------------------------------------------------
    NOSOTROS
-------------------------------------------------------------------*/

.about-main{
	background:#E6E6E6;
}
.pad-top-100{
    padding-top: 90px;
}
.pad-bottom-100{
	padding-bottom: 90px;
}

.pad-top-70{
	padding-top: 70px;
}
.pad-bottom-70{
	padding-bottom: 70px;
}

.block-title{
	font-size:52px;
	font-family: 'nautilus_pompiliusregular';
	font-weight: bold;
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