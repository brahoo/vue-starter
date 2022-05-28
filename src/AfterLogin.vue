<template>
  <div v-else>
    <h2>Witaj {{email}}</h2>
    <a @click="enter()">Wyloguj</a>
  </div>
</template>

<script>
export default {
  props: ['email'],
  methods: {
    enter() {
      this.$emit('logout');
    }
  }

}
</script>