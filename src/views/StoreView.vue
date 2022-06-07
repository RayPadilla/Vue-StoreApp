<template>
  <div class="store">
    <h1>Books</h1>
    <StoreItem />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import StoreItem from "@/components/StoreItem.vue";

@Options({
  components: {
    StoreItem,
  },
})
export default class StoreView extends Vue {}
</script>

<style scoped>
h1 {
  font-family: "Papyrus";
}
</style>
