<script setup>
import {ref} from 'vue';
// Массив товаров сгенерирован в https://dummyjson.com/
const loadedProducts =
    [
      {
        "id": 1,
        "title": "Essence Mascara Lash Princess",
        "price": 9.99,
        "description": "The Essence Mascara Lash Princess is a popular mascara known for its volumizing and lengthening effects. Achieve dramatic lashes with this long-lasting and cruelty-free formula.",
        "brand": "Essence",
        "image": "/assets/1.webp"
      },
      {
        "id": 2,
        "title": "Eyeshadow Palette with Mirror",
        "price": 19.99,
        "description": "The Eyeshadow Palette with Mirror offers a versatile range of eyeshadow shades for creating stunning eye looks. With a built-in mirror, it's convenient for on-the-go makeup application.",
        "brand": "Glamour Beauty",
        "image": "/assets/2.webp"
      },
      {
        "id": 3,
        "title": "Powder Canister",
        "price": 14.99,
        "description": "The Powder Canister is a finely milled setting powder designed to set makeup and control shine. With a lightweight and translucent formula, it provides a smooth and matte finish.",
        "brand": "Velvet Touch",
        "image": "/assets/3.webp"
      },
      {
        "id": 4,
        "title": "Red Lipstick",
        "price": 12.99,
        "description": "The Red Lipstick is a classic and bold choice for adding a pop of color to your lips. With a creamy and pigmented formula, it provides a vibrant and long-lasting finish.",
        "brand": "Chic Cosmetics",
        "image": "/assets/4.webp"
      },
      {
        "id": 5,
        "title": "Red Nail Polish",
        "price": 8.99,
        "description": "The Red Nail Polish offers a rich and glossy red hue for vibrant and polished nails. With a quick-drying formula, it provides a salon-quality finish at home.",
        "brand": "Nail Couture",
        "image": "/assets/5.webp"
      },
      {
        "id": 6,
        "title": "Calvin Klein CK One",
        "price": 49.99,
        "description": "CK One by Calvin Klein is a classic unisex fragrance, known for its fresh and clean scent. It's a versatile fragrance suitable for everyday wear.",
        "brand": "Calvin Klein",
        "image": "/assets/6.webp"
      },
      {
        "id": 7,
        "title": "Chanel Coco Noir Eau De",
        "price": 129.99,
        "description": "Coco Noir by Chanel is an elegant and mysterious fragrance, featuring notes of grapefruit, rose, and sandalwood. Perfect for evening occasions.",
        "brand": "Chanel",
        "image": "/assets/7.webp"
      },
      {
        "id": 8,
        "title": "Dior J'adore",
        "price": 89.99,
        "description": "J'adore by Dior is a luxurious and floral fragrance, known for its blend of ylang-ylang, rose, and jasmine. It embodies femininity and sophistication.",
        "brand": "Dior",
        "image": "/assets/8.webp"
      },
      {
        "id": 9,
        "title": "Dolce Shine Eau de",
        "price": 69.99,
        "description": "Dolce Shine by Dolce & Gabbana is a vibrant and fruity fragrance, featuring notes of mango, jasmine, and blonde woods. It's a joyful and youthful scent.",
        "brand": "Dolce & Gabbana",
        "image": "/assets/9.webp"
      },
      {
        "id": 10,
        "title": "Gucci Bloom Eau de",
        "price": 79.99,
        "description": "Gucci Bloom by Gucci is a floral and captivating fragrance, with notes of tuberose, jasmine, and Rangoon creeper. It's a modern and romantic scent.",
        "brand": "Gucci",
        "image": "/assets/10.webp"
      },
      {
        "id": 11,
        "title": "Annibale Colombo Bed",
        "price": 1899.99,
        "description": "The Annibale Colombo Bed is a luxurious and elegant bed frame, crafted with high-quality materials for a comfortable and stylish bedroom.",
        "brand": "Annibale Colombo",
        "image": "/assets/11.webp"
      },
      {
        "id": 12,
        "title": "Annibale Colombo Sofa",
        "price": 2499.99,
        "description": "The Annibale Colombo Sofa is a sophisticated and comfortable seating option, featuring exquisite design and premium upholstery for your living room.",
        "brand": "Annibale Colombo",
        "image": "/assets/12.webp"
      }
    ];
const products = ref(loadedProducts);

/**
 * Отправляет товар в корзину
 * @param id ID товара
 * @param e событие
 */
function toCart(id, e) {
  alert(`Метод обработки клика на кнопку зарезервирован на будущие работы.
Пока что мы передали в метод только id товара = ` + id);
}
</script>

<template>
  <section class="products">
    <article v-for="product in products" class="product-card" :key="product.id" :data-product-id="product.id">
      <img
          class="product-card__image"
          :src="product.image"
          :alt="product.title"
      >

      <div class="product-card__content">
        <p class="product-card__brand">{{product.brand}}</p>
        <h2 class="product-card__title">{{product.title}}</h2>
        <p class="product-card__description">
          {{product.description}}
        </p>

        <div class="product-card__footer">
          <span class="product-card__price">{{product.price.toLocaleString()}} ₽</span>
          <button class="product-card__button" type="button" @click="toCart(product.id, $event)">Купить</button>
        </div>
      </div>
    </article>
  </section>
</template>

<style scoped>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 40px 20px;
  font-family: Arial, sans-serif;
  background: #f5f6f8;
  color: #20232a;
}

.products {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  max-width: 1200px;
  margin: 0 auto;
}

.product-card {
  display: flex;
  flex-direction: column;
  flex: 1 1 280px;
  overflow: hidden;
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 4px 14px rgba(0, 0, 0, 0.08);
}

.product-card__image {
  display: block;
  width: 100%;
  height: 220px;
  object-fit: cover;
  background: #e9ecef;
}

.product-card__content {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  padding: 20px;
}

.product-card__brand {
  margin: 0 0 8px;
  color: #6c757d;
  font-size: 14px;
}

.product-card__title {
  margin: 0 0 12px;
  font-size: 22px;
}

.product-card__description {
  margin: 0 0 20px;
  color: #4d5359;
  line-height: 1.5;
}

.product-card__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  margin-top: auto;
}

.product-card__price {
  font-size: 22px;
  font-weight: 700;
  white-space: nowrap;
}

.product-card__button {
  padding: 11px 18px;
  border: 0;
  border-radius: 7px;
  background: #2563eb;
  color: #ffffff;
  font: inherit;
  font-weight: 700;
  cursor: pointer;
  transition: background 0.2s ease;
}

.product-card__button:hover,
.product-card__button:focus-visible {
  background: #1d4ed8;
}

@media (max-width: 600px) {
  body {
    padding: 20px 12px;
  }

  .products {
    gap: 16px;
  }
}
</style>
