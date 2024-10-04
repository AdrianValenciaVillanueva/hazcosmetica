<template>
    <div class="principal">
        <div class="imagen">
            <img src="../assets/image 4.png" alt="Imagen de cosmética" />
        </div>
        <div class="contenido">
            <div class="texto">
                <div class="titulo">
                    HAZ COSMETICA MEXICANA
                </div>
                <div class="descripcion">
                    <p class = "p1">Somos una empresa con sede en México dedicada al desarrollo de productos destacados, diseñados para destacar en los mercados más exigentes. En Haz Cosmética Mexicana, nuestra misión es proporcionar servicios y productos de alta calidad, manteniendo la mejor relación entre calidad, precio y rendimiento para satisfacer las necesidades de nuestros clientes.</p>
                    <p class = "p1">Nos comprometemos con la mejora continua en todas las áreas de nuestro negocio y nos esforzamos por brindar un servicio al cliente excepcional. Contamos con un equipo de profesionales altamente calificados que aportan sus conocimientos y experiencia a cada proyecto.</p>
                    <button class="boton">Nuestros servicios -></button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'AboutUs',  
  props: {
    className: {
      type: String,
      default: '',
    },
  },
};
</script>

<style scoped>
.principal {    
    display: flex; 
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    gap: 20px; 
}
.imagen {
    flex: .5; 
}

.imagen img {
    max-width: 85%;
    height: auto;
    border-radius: 10px;
}
.contenido {
    flex: .5; 
    padding-right: 50px;
    text-align: left;
}
.titulo {
    color: rgb(33, 37, 41);
    font-family: 'Inter', sans-serif;
    font-size: 40px;
    font-weight: 700;
    margin-bottom: 20px; 
}

.titulo::after {
    content: '';
    width: 600px;
    height: 50px;
    background-image: url('@/assets/Vector1.png'); 
    background-size: contain; 
    background-repeat: no-repeat; 
    display: block;
    margin: -1rem auto 0 auto;
  }
.p1 {
    font-family: 'Inter', sans-serif;
    font-size: 1.5vw;
    line-height: 1.5; 
    margin-bottom: 20px; 
}
.boton{
    background-color: #D9B504;
    font-family: 'Inter', sans-serif;
    border: none;
    border-radius: 8px;
    padding: 15px 30px;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
}

@media screen and (max-width: 768px) {
   .principal {
        flex-direction: column;
        align-items: center;
        align-content: center;
    }
    .contenido{
        text-align: center;
    }
    .imagen {
        display: none;
    }
    
    .contenido {
        padding: 0;
    }
    .titulo {
        font-size: 2.5em;
    }
    .p1 {
        font-size: 1.4em;
    }
    .boton {
        padding: 15px 30px;
        font-size: 1.1em;
    }
}

@media screen and (max-width: 480px) {
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .imagen {
        display: none;
    }

    .imagen img {
        display: none;
    }

    .principal {
        padding: 1.5em 0 0 0;
        margin: 0;
    }
    .contenido {
        margin: 0;
        padding: 0;
        width: 100%;
    }
    .titulo {
        text-align: center;
        margin: 0;
        padding: 0;
        font-size: 1.5rem;
    }

    .titulo::after {
    content: '';
    width: 90vw;
    height: 50px;
    background-image: url('@/assets/Vector1.png'); 
    background-size: contain; 
    background-repeat: no-repeat; 
    display: block;
    margin: -.7rem auto 0 auto;
  }

  .descripcion {
    text-align: center;
    margin: 0;
    padding: 0;
    padding-bottom:2em ;
  }

.p1 {
    text-align: center;
    margin: 0;
    padding: 0 1em;
    padding-bottom:2em ;
    font-size: 1.2em;
}

    .boton {
        padding: 3vw 6vw;
        text-align: center;
        font-size: 1.1em;
    }


}
    


</style>

