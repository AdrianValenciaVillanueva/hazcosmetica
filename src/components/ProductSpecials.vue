<template>
    <section class="product-specials">
      <h2 class="section-title">Productos especiales para ti</h2>
      <div class="product-grid">
        <ProductCard
          v-for="(product, index) in products"
          :key="index"
          :product="product"
        />
      </div>
    </section>
  </template>
  
  <script>
  import ProductCard from './ProductCard.vue';
  
  export default {
    name: 'ProductSpecials',
    components: {
      ProductCard,
    },
    data() {
      return {
        products: [
          {
            image: 'https://cdn.builder.io/api/v1/image/assets/TEMP/7ec1dbefb0b1d05f38a8a312deb5c66ff3cb34bb8c43b82b17cf0979d6f11b22?placeholderIfAbsent=true&apiKey=ead77d34b7e34f48b3fe30a77860bd44',
            category: 'Shampoos',
            name: 'Shampoo Neutro',
            price: '$85.00 – $1,000.00',
            link: 'https://hazcosmeticamexicana.com/producto/shampoo-neutro/',
          },
          {
            image: 'https://cdn.builder.io/api/v1/image/assets/TEMP/9f2f9f2b0538f1bd2674459a8014c3a9462b2eab3ac08b9e438ceab80f3c4fbf?placeholderIfAbsent=true&apiKey=ead77d34b7e34f48b3fe30a77860bd44',
            category: 'Jabones',
            name: 'Jabón Neutro Dermolimpiador',
            price: '$60.00',
            link: 'https://hazcosmeticamexicana.com/producto/jabon-neutro-dermolimpiador/',
          },
          {
            image: 'https://cdn.builder.io/api/v1/image/assets/TEMP/f1aaf4789a00a10cdbc2dda0dc48c943bf287d026ebdca373a4a6bde21d298cf?placeholderIfAbsent=true&apiKey=ead77d34b7e34f48b3fe30a77860bd44',
            category: 'Maquillajes',
            name: 'Protector Solar con Color',
            price: '$200.00',
            link: 'https://hazcosmeticamexicana.com/producto/protector-solar-con-color/',
          },
          
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .product-specials {
    border-radius: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem 1rem;
  }
  
  .section-title {
    color: #000;
    font: 600 32px Poppins, sans-serif;
    letter-spacing: 1.28px;
    margin-bottom: 2rem;
    text-align: center;
  }
  
  .product-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    width: 100%;
  }
  
  @media (max-width: 768px) {
    .product-grid {
      flex-direction: column;
      align-items: center;
    }
  
    .product-card {
      max-width: 90%;
    }
  }
  
  @media (min-width: 769px) and (max-width: 1024px) {
    .product-card {
      max-width: 45%;
    }
  }
  
  @media (min-width: 1025px) {
    .product-card {
      max-width: 30%;
    }
  }
  </style>