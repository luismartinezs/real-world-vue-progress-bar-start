<template>
  <div>
    <h1>Uh-oh!</h1>
    <p>It loks like you're experience some network isues, trye again</p>
    <router-link :to="{ name: 'event-list' }">Back to home</router-link>
  </div>
</template>