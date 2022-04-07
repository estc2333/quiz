<template>
  <div class="questions-ctr">
    <div class="progress">
      <div class="bar"></div>
      <div class="status">1 out of 3 questions answered</div>
    </div>
    <div class="single-question" v-for="(question, index) in questions" :key="question.q" v-show="index === questionsAnswered">
      <div class="question"> {{question.q}}</div>
      <div class="answers" v-for="answer in question.answers" :key="answer.text">
        <div class="answer" >{{answer.text}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Questions',
  props: {
    questions: {
      type: Array,
      default: () => ([])
    },
    questionsAnswered: {
      type: Number,
      default: 0,
    },
  },
  data() {
    return {
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
