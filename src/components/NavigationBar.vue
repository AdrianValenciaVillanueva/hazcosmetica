<template>
  <div :class="['navigation-bar', className]">
    <div class="logo">
      <img class="image" alt="Image" src="../assets/logo.png" />
      <p>HAZ COSMETICA MEXICANA</p>
      <button :class="['hidden-menu', { 'menu-open': isMenuVisible }]" @click="toggleMenu">
        <i class="fas fa-bars"></i>
      </button>
    </div>
    <div :class="['frame', { 'frame-visible': isMenuVisible }]">
      <button class="text-wrapper">Inicio</button>
      <button class="text-wrapper">Nuestra Marca</button>
      <button class="text-wrapper">Servicios</button>
      <button class="text-wrapper">Tienda</button>
      <button class="text-wrapper" id="carrito">
        <i class="fas fa-shopping-cart"></i>
      </button>
      <button class="text-wrapper" id="contacto">Contacto</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavigationBar',
  
  props: {
    className: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      isMenuVisible: true,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuVisible = !this.isMenuVisible; // Cambia el estado
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jomolhari&display=swap');



.navigation-bar {
  align-items: center;
  box-shadow: 0px 4px 4px #00000040;
  display: flex;
  justify-content: space-between;
  padding: 0 5vw;
  position: relative;
  width: 100%;
  box-sizing: border-box;
  background-color: #3f5905;
}

.logo {
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.navigation-bar .image {
  height: 3vw;
  width: auto;
}

.navigation-bar .logo p {
  font-family: 'Jomolhari', serif;
  font-size: 1.5vw;
  color: #fff;
}

.navigation-bar .frame {
  display: flex;
  width: auto;
  padding: .5em;
  flex-direction: row;
  align-items: center;
  gap: 2vw;
  overflow: hidden;
  max-height: 0; /* Inicialmente oculto */
  opacity: 0; /* Comienza oculto */
  transition: max-height 0.4s ease-in-out, opacity 1s ease-in-out; /* Transición más rápida */
}

.navigation-bar .frame.frame-visible {
  max-height: 300px; /* Valor ajustado, asegúrate de que sea suficiente para tu contenido */
  opacity: 1; /* Hacer visible el contenido */
}

.hidden-menu {
  background: none;
  border: none;
  color: #fff;
  cursor: pointer;
  margin: 20px;
  padding: 0;
  font-size: 1.1em;
  display: none; /* Ocultar por defecto */
  transition: color 0.3s ease, transform 0.6s ease; /* Añadir transición */
}

.hidden-menu.menu-open {
  transform: rotate(90deg); /* Rotar cuando el menú está abierto */
}

.hidden-menu:hover,
.hidden-menu:focus {
  color: #F2E205;
}

.navigation-bar .text-wrapper {
  color: #A4A5A6;
  font-family: 'Space Grotesk-Regular', Helvetica;
  font-size: 1.5vw;
  font-weight: 400;
  line-height: 28px;
  position: relative;
  white-space: nowrap;
  width: fit-content;
  transition: color 0.3s ease, transform 0.3s ease;
  padding: 10px 1.2vw;
  background-color: transparent;
  border: none;
  box-shadow: none;
}

.navigation-bar .text-wrapper:hover, 
.navigation-bar .text-wrapper:focus {
  color: #F2E205;
  cursor: pointer;
}

#contacto {
  color: #000000;
  padding-left: 15px;
  background: #D9B504;
  padding-left: 22px;
  padding-right: 22px;
  padding-top: 17px;
  padding-bottom: 17px;
  border-radius: 10px;
  font-family: 'Jomolhari', serif;
  transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease; 
}

#contacto:hover, 
#contacto:focus {
  background-color: #A3A646;
  color: #1e1e1e;
  transform: scale(1.05);
}

#carrito { 
  color: #A3A646;
  border: 2px solid #A3A646;
  padding-left: 22px;
  padding-right: 22px;
  padding-top: 19px;
  padding-bottom: 19px;
  border-radius: 10px;
  transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease;
  display: inline-flex; 
  align-items: center;  
}

#carrito:hover, 
#carrito:focus {
  background-color: #A3A646;
  color: #1e1e1e;
  transform: scale(1.05); 
}

/* Media queries para ajustar el tamaño de la fuente y otros estilos en diferentes tamaños de pantalla */
@media (max-width: 1200px) {
  .navigation-bar {
    align-items: center;
    justify-content: space-around;
    display: flex;
    padding: 0;
    width: 100%;
  }
  
  .navigation-bar .text-wrapper {
    font-size: 2vw;
    margin: 0;
  }

  .logo {
    display: flex;
    align-items: center;
    padding-left: 1em;
  }

  .navigation-bar .image {
    height: 4vw;
  }

  .navigation-bar .frame {
    gap: 1vw;
    justify-content: space-between;
    padding-right: 1em;
  }
}

@media (max-width: 768px) {
  .navigation-bar {
    padding-top: 10px;
    gap: 0;
    display: flex;
    flex-direction: column;
  }
 
  .navigation-bar .text-wrapper {
    font-size: 2.4vw;
  }

  .logo img {
    max-height: 35px;
  }

  .navigation-bar .logo p {
    font-family: 'Jomolhari', serif;
    font-size: 1em;
  }

  .navigation-bar .image {
    height: 6vw;
  }

  .navigation-bar .frame {
    display: flex;
    justify-content: space-around;
  }

  #contacto {
    padding: .5em;
    font-size: 1.8vw;
    min-height: 35px;
  }

  #carrito {
    padding: .6em;
    min-height: 37px;
  }
}

@media (max-width: 530px) {
  .navigation-bar {
    display: flex;
    padding: 0;
  }

  .hidden-menu {
    display: flex;
  }

  .navigation-bar .frame {
    max-height: 0;
    padding: 0em;
    opacity: 0; 
    width: 100%;
    transition: max-height 0.6s ease-in-out, opacity 0.6s ease-in-out;
  }

  .navigation-bar .frame.frame-visible {
    max-height: 500px; 
    opacity: 1; 
  }

  .navigation-bar .text-wrapper {
    font-size: 3vw;
    padding: 8px 8px; /* Asegura que todos los botones tengan el mismo padding */
  }

  .navigation-bar .image {
    height: 0;
    display: none;
  }

  #contacto {
    font-family: 'Jomolhari', serif;
    font-size: 2.5vw;
    color: #000000;
    letter-spacing: .1em;
    padding: 5px 5px;
    margin-right: 1.3vw;

  }
  #carrito {
    padding: 10px;
    display: flex;
    align-items: center; /* Asegura que el ícono del carrito esté centrado verticalmente */
    justify-content: center; /* Centrar horizontalmente */
    margin: 0; /* Asegurar que no haya margen lateral */
  }

  
}
</style>