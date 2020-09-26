<template>
  <div>
    <b-jumbotron>
      <template slot:lead> </template>
      <p v-html="currentQuestion.question"></p>
      <hr class="my-4" />

      <p>{{ currentQuestion.correct_answer }}</p>

      <b-button variant="primary" href="#">Submit</b-button>
      <b-button @click="next" variant="success" href="#"> Next </b-button>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  props: {
    currentQuestion: Object,
    next: Function,
  },
};
</script>