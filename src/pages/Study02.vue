<template>
  <div>
    <p>{{firstNumber}}곱하기{{secondNumber}}는 몇?</p>
    <form v-on:submit="onSubmitForm">
      <input type="number" ref="answer" v-model="value" />
      <button type="submit">입력</button>
    </form>
    <div id="result">{{result}}</div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      firstNumber: Math.ceil(Math.random() * 9),
      secondNumber: Math.ceil(Math.random() * 9),
      result: "",
      value: ""
    };
  },
  methods: {
    onSubmitForm(e) {
      e.preventDefault();
      if (this.firstNumber * this.secondNumber === parseInt(this.value)) {
        this.firstNumber = Math.ceil(Math.random() * 9);
        this.secondNumber = Math.ceil(Math.random() * 9);
        this.$refs.answer.focus();
        this.result = "정답입니다.";
        this.value = "";
      } else {
        this.result = "오답입니다.";
        this.value = "";
      }
    }
  }
};
</script>

<style>
</style>