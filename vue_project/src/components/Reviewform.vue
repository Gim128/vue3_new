<template>
  <Card>
    <form @submit.prevent="handleSubmit">
      <h2>How would you rate your service with us?</h2>
      <!-- Rating component -->

      <RatingSelect :rating="rating" @setRating="setRating" />

      <div class="input-group">
        <input type="text" placeholder="Write a review" v-model="Text" />
        <button type="submit" class="btn btn-primary" :disabled="btnDisabled"></button>
      </div>
      <div class="message">Text must be at least 15 Characters</div>
    </form> </Card
  >>
</template>

<script setup>
import { ref } from "vue";
import Card from "./CardComponent.vue";
import RatingSelect from "./RatingSelect.vue";
import { useReviewStore } from "../stores/review";

const store = useReviewStore();
const text = ref("");
const btnDisabled = ref(false);
const message = ref("");
const rating = ref(10);

const handleSubmit = () => {
  const newReview = {
    text: text.value,
    rating:rating.value,
  };

  if(!store.editedContent.editable){
    store.addReview(newReview);
  }else{
    store.updateReview({
      ...newReview,
      id: store.editedContent.item.id,
    })
  }
}

const setRating = (val) => {
  rating.value = val;
  console.log(val);
};
</script>

<style scoped></style>
