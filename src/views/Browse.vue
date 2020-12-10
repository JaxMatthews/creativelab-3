<template>
<div>
  <h1> Movies I Would Not Watch </h1>
  <RemoveList2 :movies="would" />
</div>
</template>

<script>
import RemoveList2 from "../components/RemoveList2.vue"
export default {
  name: 'Yes',
  components: {
    RemoveList2
  },
  data() {
    return{

    }
  },
  computed: {
    would() {
      return this.$root.$data.aYes;
    }
  },
  methods: {

  }
  }
</script>
