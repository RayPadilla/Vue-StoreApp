<template>
  <div class="home">
    <ul>
      <li v-for="book in books" :key="book">
        <h2>{{ book.title }}</h2>
        <p>{{ book.author }}</p>
      </li>
    </ul>
    <button @click="changeTitle('Dune')">Button</button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },

  data() {
    return {
      books: [
        { title: "The Final Empire", author: "Author 1" },
        { title: "Dune", author: "Author 2" },
        { title: "The Lightning Thief", author: "Author 3" },
      ],
    };
  },
  methods: {
    /*changeTitle(x: number) {
      this.books[x] = books[x];
    },*/
  },
})
export default class HomeView extends Vue {}
</script>
