<template>
    <div class="services-section">
      <h2 class="services-title">Servicios</h2>
      <div class="services-block">
        <div class="service-card" v-for="(service, index) in services" :key="index">
          <div class="service-card-content">
            <h3 class="service-title">{{ service.title }}</h3>
            <p class="service-description">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ServicesBlock',
    data() {
      return {
        services: [
          {
            title: 'Identidad de Marca:',
            description: 'Creamos una imagen coherente para tu marca, desde logotipos hasta sitios web. Te ayudamos a desarrollar diseños únicos que te destaquen, trabajando contigo en cada etapa para asegurar tu éxito.'
          },
          {
            title: 'Catálogo de productos:',
            description: 'Ofrecemos productos con formulaciones comprobadas y posición sólida en el mercado. Tú eliges el producto, envase y logotipo, ¡listo para destacar!'
          },
          {
            title: 'Diseño de envases personalizado:',
            description: 'Dispones de una variedad de envases y etiquetas personalizables. Nuestro equipo colabora contigo para garantizar un diseño perfecto, con muestras para tu aprobación antes de la producción final. Tu satisfacción es nuestra prioridad.'
          },
          

        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* Importar la fuente Inter desde Google Fonts */
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');
  
 
  .services-section {
    font-family: 'Inter', sans-serif;
    text-align: center;
    padding: 2rem 5vw;
  }
  
  .services-title {
    font-size: 2rem;
    font-weight: 700; /* Negrita */
    position: relative;
    display: inline-block;
    margin-bottom: 1rem;
  }
  
  .services-title::after {
    content: '';
    width: 150px;
    height: 50px;
    background-image: url('@/assets/Vector.png'); 
    background-size: contain; 
    background-repeat: no-repeat; 
    display: block;
    margin: -1rem auto 0 auto;
  }
  
  
  /* Estilos para las tarjetas de servicio */
  .service-card {
    width: 90%;
    background-color: #f8f8f8;
    border-radius: 10px;
    padding: 1.5rem;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  .service-card-content {
    padding: 1rem;
  }
  
  .service-title {
    font-size: 1.5rem;
    font-weight: 700; /* Negrita */
    margin-bottom: 0.5rem;
  }
  
  .service-description {
    font-size: 1rem;
    color: #1b1c1c;
    font-weight: 400; 
  }
  
  /* Estilos para el bloque de servicios */
  .services-block {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    justify-items: center;
  }
  
  /* Media query para dispositivos móviles */
  @media (max-width: 900px) {
    .services-block {
      grid-template-columns: repeat(1, 1fr);
    }
  }
  </style>
  