<template>
  <nav class="">
    <div class="text-center w-100 py-4" >
      <h1 class="bold">Conoce Comala</h1>
    </div>
  </nav>
  <div class="d-flex px-5 bg-gray py-3" style="justify-content: space-evenly;">
      <button class="btn btn-p">
        Hoteles
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-home"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path><polyline points="9 22 9 12 15 12 15 22"></polyline></svg>
      </button>
      <button class="btn btn-p">
        Cosas que hacer
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-map-pin"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path><circle cx="12" cy="10" r="3"></circle></svg>
      </button>
      <button class="btn btn-p">
        Restaurantes
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-coffee"><path d="M18 8h1a4 4 0 0 1 0 8h-1"></path><path d="M2 8h16v9a4 4 0 0 1-4 4H6a4 4 0 0 1-4-4V8z"></path><line x1="6" y1="1" x2="6" y2="4"></line><line x1="10" y1="1" x2="10" y2="4"></line><line x1="14" y1="1" x2="14" y2="4"></line></svg>
      </button>
      <button class="btn btn-p">
        Tours
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-map"><polygon points="1 6 1 22 8 18 16 22 23 18 23 2 16 6 8 2 1 6"></polygon><line x1="8" y1="2" x2="8" y2="18"></line><line x1="16" y1="6" x2="16" y2="22"></line></svg>
      </button>
      <button class="btn btn-p">
        Foros de viaje
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-message-square"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path></svg>
      </button>
    </div>
  <HelloWorld/>
  <footer>
    <div class="row px-3 py-3">
      <div class="col-md-6">
        <div class="mb-3" style=" width: 100px; height: 100px;">
          <img  src="/img/conocecomala.png" alt="conoce comala">
        </div>
        <h2>CONOCE COMALA</h2>
        <div class="d-flex" style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-map-marker"></i> <p class="ml10 mb-0">Calle Loma Alta 41</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-phone"></i> <p class="ml10 mb-0">+52 312-3017-517</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-envelope"></i> <p class="ml10 mb-0">conoce.comala@gmail.com</p>
        </div>
        <div class="d-flex"  style="align-items: center; margin-bottom: .5rem;">
          <i class="pi pi-facebook"></i> <p class="ml10 mb-0">Conoce Comala</p>
        </div>
        
      </div>
      <div class="col-md-6">
        <p>En estos momentos nos encontramos en la fase Betta del sitio web estamos trabajando en la version 1.0.</p>
      </div>
    </div>
    
  </footer>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dosis:wght@200;300;400;500;600;700;800&family=Quicksand:wght@300;400;500;600;700&family=Roboto:ital,wght@0,100;0,300;1,100;1,300&display=swap');
#app{
  overflow-y: hidden;
  font-family: 'Roboto', sans-serif;
  color:  #7c553e 
}
h1,h2,h3,h4,h5,h6 {
  font-family: 'Dosis', sans-serif;
  color:  #643c24 ;
}
.bg-gray{
  background: #d3bba3;
}
nav, footer{
  position: sticky;
    top: 0;
    background: #faecde;;
    z-index: 109;
}

</style>
