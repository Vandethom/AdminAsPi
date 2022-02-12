<template>
  <div>
    <SearchBar />
    <SideBar />
  </div>
</template>

<script>
import SearchBar from '~/components/SearchBar.vue'
import SideBar from '~/components/SideBar.vue'

export default {
  name: 'Index',

  components: {
    SearchBar,
    SideBar
  }
}
</script>


<style>
  body {
    margin: 0;
  }
</style>
