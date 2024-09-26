<template>
  <div :class="['navigation-bar', className]">
    <div class="logo">
      <img class="image" alt="Image" src="../assets/logo.png" />
      <p>HAZ COSMETICA MEXICANA</p>
    </div>
    <div class="frame">
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
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jomolhari&display=swap');

*{
  box-sizing: border-box;
}
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
  gap: 1vw;
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
  align-items:center;
  display: flex;
  flex-direction:row;
  gap: 2vw;
  
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
  transition: color 0.3s ease, color 0.3s ease, transform 0.3s ease;
  padding: 10px 20px;
  background-color: transparent;
  border:none;
  box-shadow: none;
  
}
.navigation-bar .text-wrapper:hover , .navigation-bar .text-wrapper:focus {
  color: #F2E205;
  cursor: pointer;
}

#contacto {
  color: #000000;
  padding-left: 15px;
  background: #D9B504;
  padding-left: 22px;
  padding-right: 22px;
  padding-top: 19px;
  padding-bottom: 19px;
  border-radius: 10px;
  transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease; 
}
#contacto:hover, #contacto:focus {
  background-color:#A3A646;
  color: #1e1e1e;
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

#carrito:hover, #carrito:focus {
  background-color: #A3A646;
  color: #1e1e1e;
  transform: scale(1.05); 
}



/* Media queries para ajustar el tamaño de la fuente y otros estilos en diferentes tamaños de pantalla */
@media (max-width: 1200px) {
  
  .navigation-bar .text-wrapper {
    font-size: 2vw;
  }

  .navigation-bar .image {
    height: 6vw;
  }

  .navigation-bar .frame {
    gap: 3vw;
  }
  
}

@media (max-width: 768px) {
  .navigation-bar{
    gap: 8vw;
  }
  .navigation-bar .text-wrapper {
    font-size: 2.4vw;
  }

  .navigation-bar .image {
    height: 6vw;
  }

  .navigation-bar .frame {
    gap: 1.5vw;;
  }
  #contacto {
    margin-top: .35vw;
    padding-left: 1.4vw;
    padding-right: 1.4vw;
    padding-top: .8vw;
    padding-bottom: .8vw;
  }
}

@media (max-width: 530px) {
  .navigation-bar{
    gap: 0;
  }
  .navigation-bar .text-wrapper {
    font-size: 3.5vw;
  }

  .navigation-bar .image {
    height: 0;
  }

  .navigation-bar .frame {
    gap: 0;
  }
  #contacto {
    margin-top: 1vw;
    padding-left: 1.5vw;
    padding-right: 1.5vw;
    padding-top: .8vw;
    padding-bottom: .8vw;
  }
}

</style>