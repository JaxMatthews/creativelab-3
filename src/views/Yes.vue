<template>
<div>
  <h1> Movies I Would Not Watch </h1>
  <RemoveList :movies="wouldNot" />
</div>
</template>

<script>
import RemoveList from "../components/RemoveList.vue"
export default {
  name: 'Yes',
  components: {
    RemoveList
  },
  data() {
    return{

    }
  },
  computed: {
    wouldNot() {
      return this.$root.$data.aNo;
    }
  },
  methods: {

  }
  }
</script>
