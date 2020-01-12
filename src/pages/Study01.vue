<template>
  <div>
    <p v-if="liked">좋아요 Liked</p>
    <button type="button" v-else @click="actionBtnLike">LIKE</button>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      liked: false
    };
  },
  methods: {
    actionBtnLike() {
      this.liked = true;
    }
  }
};
</script>

<style>
</style>