<template>
    <article class="product-card">
      <div class="product-image-wrapper">
        <img :src="product.image" :alt="product.name" class="product-image" />
      </div>
      <div class="product-info">
        <div class="product-details">
          <h3 class="product-category">{{ product.category }}</h3>
          <p class="product-name">
            <a v-if="product.link" :href="product.link" class="product-link" target="_blank" rel="noopener noreferrer">
              {{ product.name }}
            </a>
            <span v-else>{{ product.name }}</span>
            <br />
            <span class="product-price">{{ product.price }}</span>
          </p>
        </div>
        <button class="add-to-cart-btn" aria-label="Add to cart">
          <img src="https://cdn.builder.io/api/v1/image/assets/TEMP/f49f02113eab500e68afd219a798f5feab8f4e0ea85a466b5b9591f237ebb7a5?placeholderIfAbsent=true&apiKey=ead77d34b7e34f48b3fe30a77860bd44" alt="" class="cart-icon" />
        </button>
      </div>
    </article>
  </template>
  
  <script>
  export default {
    name: 'ProductCard',
    props: {
      product: {
        type: Object,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .product-card {
    border-radius: 12px;
    background-color: #fff;
    display: flex;
    flex-direction: column;
    padding: 20px;
    width: 100%;
    max-width: 300px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .product-image-wrapper {
    border-radius: 12px;
    overflow: hidden;
  }
  
  .product-image {
    aspect-ratio: 1.44;
    object-fit: cover;
    width: 100%;
  }
  
  .product-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }
  
  .product-details {
    font-family: Poppins, sans-serif;
    color: #25261f;
    font-weight: 600;
    text-align: center;
  }
  
  .product-category {
    font-size: 18px;
    letter-spacing: 0.96px;
  }
  
  .product-name {
    font-size: 16px;
    letter-spacing: 0.8px;
    margin-top: 10px;
  }
  
  .product-link {
    text-decoration: underline;
    color: #25261f;
  }
  
  .add-to-cart-btn {
    border-radius: 50%;
    background-color: #6f8c04;
    display: flex;
    height: 45px;
    width: 45px;
    align-items: center;
    justify-content: center;
    padding: 10px;
    border: none;
    cursor: pointer;
    margin-top: 20px;
  }
  
  .cart-icon {
    width: 18px;
  }
  
  @media (max-width: 991px) {
    .product-card {
      width: 100%;
      padding: 20px;
    }
  
    .product-info {
      margin-top: 20px;
    }
  
    .add-to-cart-btn {
      margin-top: 20px;
    }
  }
  </style>