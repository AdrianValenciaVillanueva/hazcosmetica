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
    display: flex; /* Usamos flexbox para alinear la imagen y el contenido en una fila */
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    gap: 20px; /* Añadimos un espacio entre la imagen y el contenido */
}
.imagen {
    flex: 1; /* La imagen ocupará el 50% del ancho de la caja principal */
}

.imagen img {
    max-width: 100%; /* La imagen no saldrá de su contenedor */
    height: auto;
    border-radius: 10px;
}
.contenido {
    flex: 1; /* El contenido ocupará el otro 50% del ancho de la caja principal */
    text-align: left;
}
.titulo {
    color: rgb(33, 37, 41);
    font-family: 'Inter', sans-serif;
    font-size: 40px;
    font-weight: 700;
    margin-bottom: 20px; /* Espacio debajo del título */
}
.p1 {
    font-family: 'Inter', sans-serif;
    font-size: 18px;
    line-height: 1.5; /* Mejora la legibilidad con espacio entre líneas */
    margin-bottom: 20px; /* Espacio debajo de cada párrafo */
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

</style>

