<template>

  <div class="ui centered card">
    <div class="content" v-on:click="viewQuiz(quiz)">
      <div class="header">
        {{quiz.title}}
      </div>
      <div class="meta">
        {{quiz.description}}
      </div>
    </div>
    <div class="extra content">
      <span class="left floated">
        <i class="sticky note icon"></i>
        {{quiz.cards.length}}
      </span>
      <span class="right floated" v-on:click="deleteQuiz(quiz)">
        <i class="trash icon"></i>
      </span>
    </div>
  </div>

</template>


<script>

  export default {
    props: ['quiz'],
    methods: {
      viewQuiz(quiz) {
        this.$emit('view-quiz', quiz);
      },
      deleteQuiz(quiz) {
        this.$emit('delete-quiz', quiz);
      }
    }
  }

</script>

<style>

</style>
