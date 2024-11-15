<template>
  <q-page class="flex flex-center">
    <BookContent />
  </q-page>
</template>

<script>
import BookContent from "../components/BookContent.vue";
export default {
  name: "BookPage",
  components: {
    BookContent,
  },
};
</script>
