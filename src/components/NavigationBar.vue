<template>
  <div :class="['navigation-bar', className]">
    <div class="logo">
      <img class="image" alt="Image" src="../assets/logo.png" />
      <p>HAZ COSMETICA MEXICANA</p>
    </div>
    <div class="frame">
      <button class="text-wrapper">Inicio</button>
      <button class="text-wrapper">Servicios</button>
      <button class="text-wrapper">Nosotros</button>
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

.navigation-bar {
  align-items: center;
  box-shadow: 0px 4px 4px #00000040;
  display:inline-flex;
  gap: 15vw;
  padding-left: 5vw;
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
  position: relative;
  width: auto;
}

.navigation-bar .logo p {
  
  font-family: 'Jomolhari', serif;
  font-size: 1.5vw;
  color: #fff;
  
}

.navigation-bar .frame {
  align-items:flex-start;
  display: flex;
  flex-direction:row;
  gap: 6vw;
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
  color: #F2E205;
  border: #F2E205, 2px, solid;
  padding-left: 15px;
  padding-right: 15px;
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 10px;
  transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease; 
}
#contacto:hover, #contacto:focus {
  background-color: #F2E205;
  color: #1e1e1e;
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