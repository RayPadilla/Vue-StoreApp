<template>
  <div class="container">
    <div v-for="book in books" :key="book" class="grid-item">
      <h2>{{ book.title }}</h2>
      <img :src="book.src" />
      <p>{{ book.author }}</p>
      <p>{{ book.release }}</p>
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
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1617768316l/68428._SY475_.jpg",
        },
        {
          title: "Dune",
          author: "Frank Herbert",
          release: "August 1965",
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1555447414l/44767458.jpg",
        },
        {
          title: "The Lightning Thief",
          author: "Rick Riordan",
          release: "June 2005",
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1400602609l/28187.jpg",
        },
        {
          title: "The Hobbit",
          author: "J.R.R Tolkien",
          release: "January 1937",
          src: "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1546071216l/5907.jpg",
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
  padding: 0 25px 0 25px;
}

.grid-item {
  grid-column: span 1;
  grid-row: span 1;
  background-color: #334195;
  color: white;
  align-items: center;
  box-shadow: 2.5px 2.5px 3px 3px rgba(0, 0, 0, 0.3);
}

img {
  width: 150px;
  height: 220px;
}

button {
  margin: 5px;
}
</style>
