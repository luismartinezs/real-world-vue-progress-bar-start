<template>
  <p>{{ comment | reply('bro') | shout | exclaim }}</p>
</template>

<script>
export default {
  data() {
    return {
      comment: 'no one cares',
    }
  },
  filters: {
    shout(value) {
      return value.toUpperCase()
    },
    exclaim(value) {
      return value + '!!!'
    },
    reply(value, name) {
      return value + ', ' + name
    },
  },
}
</script>
