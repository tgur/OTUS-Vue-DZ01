<script setup>

// Массив товаров сгенерирован в https://dummyjson.com/
const products =
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


</script>

<template>
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>

</template>

<style scoped></style>
