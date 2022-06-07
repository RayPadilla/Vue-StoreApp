<template>
  <div class="container">
    <div v-for="book in books" :key="book" class="grid-item">
      <h2>{{ book.title }}</h2>
      <img :src="book.src" />
      <p class="author">{{ book.author }} - {{ book.release }}</p>
      <p class="price">${{ book.price }}</p>
      <button>Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      books: [
        {
          title: "The Final Empire",
          author: "Brandon Sanderson",
          release: "July 2006",
          price: 9.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1617768316l/68428._SY475_.jpg",
        },
        {
          title: "Dune",
          author: "Frank Herbert",
          release: "August 1965",
          price: 10.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1555447414l/44767458.jpg",
        },
        {
          title: "The Lightning Thief",
          author: "Rick Riordan",
          release: "June 2005",
          price: 11.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1400602609l/28187.jpg",
        },
        {
          title: "The Hobbit",
          author: "J.R.R Tolkien",
          release: "January 1937",
          price: 12.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1546071216l/5907.jpg",
        },
        {
          title: "Animal Farm",
          author: "George Orwell",
          release: "August 1945",
          price: 13.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1325861570l/170448.jpg",
        },
        {
          title: "Twilight",
          author: "Stephanie Meyer",
          release: "October 2005",
          price: 14.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1361039443l/41865.jpg",
        },
        {
          title: "Harry Potter and The Sorcerer's Stone",
          author: "J.K. Rowling",
          release: "June 1997",
          price: 15.99,
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1474154022l/3._SY475_.jpg",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  grid-auto-rows: minmax(300px, auto);
  padding: 0 25px 25px 25px;
}

.grid-item {
  grid-column: span 1;
  grid-row: span 1;
  background-color: #ffe6a7;
  color: black;
  align-items: center;
  box-shadow: 2.5px 2.5px 3px 3px rgba(0, 0, 0, 0.3);
}

h2 {
  color: black;
  font-family: "Copperplate";
}

.author {
  font-weight: bold;
  font-size: 20px;
  font-family: "Times New Roman";
}

.price {
  font-family: "Courier New";
  font-weight: bold;
}

img {
  width: 150px;
  height: 220px;
  transition: all 0.5s;
  border: 2px solid black;
}

img:hover {
  transform: scale(1.1);
}

button {
  margin: 5px;
}
</style>
