<template>
  <div class="container-fluid pt-3 bg-gray">
    <div class="row">
      <div class="col-md-12">
        <h2 class="text-center principal-text mb-4">Conoce los mejores restaurantes de Comala</h2>
        <div class="row">
          <div v-for ="item in testament" :key="item.id" class="col-md-3 text-center">
            <div class="card m-a" style="width: 18rem;">
              <img :src="item.img" class="card-img-top">
              <div class="card-body">
                <h5 class="card-title">{{item.nombre}}</h5>
                <p class="card-text">{{item.direccion}}</p>
                <button 
                class="btn-p"
                @click="abrirModalInfo(item)"
                >
                  Conoce
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-right"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
                </button>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-9 my-5 m-a">
          <div class="container-card">
            <div class="row">
              <div class="col-md-6">
                <div class="p-3">
                  <h4 class="mb-5">Ven y conoce los lugares para <b>conectar con Comala</b></h4>

                  <p><b>+ 1000</b> lugares magicos por concer en Comala...</p>
                  <div class="text-center w-100 mt-5">
                    <button class="btn-p">
                      Conoce
                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-right"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
                    </button>
                  </div>
                  
                </div>
                
              </div>
              <div class="col-md-6">
                <div class="img-cont">
                  <img class="img" src="/img/mig2.jpg" alt="">
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <h3 class="text-center principal-text mb-5">Galeria</h3>
          <div class="row">
            <div v-for="img in imgs" :key="img.id" class="col-md-3 mb-4">
            <div class="img-cont">
              <img :src="img.img" alt="">
            </div>
            </div>

          </div>
        </div>
      </div>
    </div>
    <Dialog 
    :header="testmodal.nombre" 
    v-model:visible="open" 
    :breakpoints="{'960px': '75vw', '640px': '90vw'}" 
    :style="{width: '70vw'}">
      <div class="px-2 py-3">
        <div class="d-flex" style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-map-marker"></i> <p class="ml10 mb-0">{{testmodal.direccion}}</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-phone"></i> <p class="ml10 mb-0">{{(testmodal.telefono) ? testmodal.telefono:'--'}}</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-envelope"></i> <p class="ml10 mb-0">{{(testmodal.correo) ? testmodal.correo:'--'}}</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-facebook"></i> <p class="ml10 mb-0">{{testmodal.facebook}}</p>
        </div>
        <div>
          <p class="bold" style="margin-bottom: .5rem;">Descripción</p>
          <p style="margin-bottom: .5rem;">{{testmodal.desc}}</p>
        </div>
        <p class="bold" style="margin-bottom: .5rem;">Calificación</p>
        <div class="d-flex">
          <i class="pi pi-star-fill"></i> 
          <i class=" mx-2 pi pi-star-fill"></i> 
          <i class="pi pi-star-fill"></i> 
          <i class="mx-2 pi pi-star-fill"></i> 
          <i class="pi pi-star"></i> 
        </div>
        
      </div>
    </Dialog>

  </div>
</template>
<script>
import 'primeicons/primeicons.css';
import Dialog from 'primevue/dialog';
export default {
  components:{
    Dialog,
  },
  data(){
    return {
      open: false,
      testmodal: [],
      testament: [
        {
          id: 1,
          nombre: 'Casa pascual del Rio',
          direccion: '5 de Mayo, Centro, Comala, Colima',
          telefono: '',
          facebook: 'Casa pascual del Rio',
          correo:'pascualgastronomia@gmail.com',
          img: '/img/casa1.jpg',
          desc: 'Casa Pascual del Río. Residencia de exploración gastronómica, artística y cultural del chef Ala'
        },
        {
          id: 2,
          nombre: 'Campestre San Martin',
          direccion: 'Km 6.5 Carretera Comala a, 28459 Suchitlán, Col.',
          telefono: '+52 312-3954-623',
          img: '/img/campestre2.jpg',
          facebook: 'Campestre San Martin',
          correo:'',
          desc:"Campestre los Pinos somos un restaurante que combina por una parte la exquisitez de los platillos típicos regionales de Colima con nuestra propia versión de ellos, lo que hacer a nuestra cocina gran experiencia. Aquí los niños se recrean jugando y liberando su energía en un entorno natural, rodeados de robustos pinos, frondosas parotas y flores multicolor; enclavado a solo unos minutos de Colima. Ven y déjanos consentirte"
        },
        {
          id: 3,
          nombre: 'Los portales Suchitlan',
          direccion: 'Galeana 10, Centro, 28459 Suchitlán, Col.',
          telefono: '+52 312-3954-452',
          img: '/img/portales3.jpg',
          facebook: 'Los portales Suchitlan',
          correo:'',
          desc:'Disfruta nuestros deliciosos platillos en un hermoso lugar rodeado de arboles!!! Restaurant Campestre Suchitlán- Colima'
        },
        {
          id: 4,
          nombre: 'Tiro Loco',
          direccion: 'Capitán Llerenas 22, Centro, 28450 Comala, Col.',
          telefono: '+52 312-3155-980',
          img: '/img/tiroloco4.jpg',
          facebook: 'restaurante Tiriloco',
          correo:'',
          desc:'Comida rapida . . . Tortas,Hamburguesas,Hot Dogs,Gringas,Sincronizadas,Burritos y más!!!'
        },
      ],
      imgs: [
        {
          id: 1,
          img: '/img/1.jpg',
        },
        {
          id: 2,
          img: '/img/2.jpg',
        },
        {
          id: 3,
          img: '/img/3.jpg',
        },
        {
          id: 4,
          img: '/img/4.jpg',
        },
        {
          id: 5,
          img: '/img/5.jpg',
        },
        {
          id: 6,
          img: '/img/6.jpg',
        },
        {
          id: 7,
          img: '/img/mig2.jpg',
        },
        {
          id: 8,
          img: '/img/7.jpg',
        },
      ],
    }
  },
  methods: {
    abrirModalInfo(item) {
      this.open = true;
      this.testmodal = item;
      console.log(item)

    }
  }
}
</script>

<style>
.bold{
  font-weight: bold !important;
}
.ml10{
  margin-left: 10px;
}
.card-text{
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
}
.m-a{
  margin: auto;
}
.principal-text{
  font-weight: bold;
  /* font-size: 18px; */
}
.container-card{
  background: white;
  border-radius: 10px;
  box-shadow: 10px 3px 29px -13px rgba(0,0,0,0.72);
}
/*Supongamos que nuestro contenedor mide 150px x 150px*/
.img{
  /* width:150px; */
  height:300px;
}
/*Aplicamos la propiedad object-fit cover, ajustar su tamaño y no perder la proporcion de nuestra imagen*/
img{
  object-fit: cover;
  width:100%;
  height:100%;
}
.btn-p{
  border: 2px solid  #926d55  !important;
  font-size: 18px !important;
  font-weight: bold !important;
  border-radius: 10px !important;
  padding: 5px 15px !important;
  color: #926d55 !important;
  background-color: #faecde;
}

.btn-p:hover{
  background: #9c7c6c;
  color: #d3bba3  !important;
}

.p-dialog-mask {
    background: rgba(0, 0, 0, 0.8);
  }
.p-dialog {
    background: white;
    padding: 15px;
}
.p-dialog-title{
  font-family: 'Dosis', sans-serif;
  color:  #643c24 ;
  font-size: 20px;
  font-weight: bold;
}



</style>
