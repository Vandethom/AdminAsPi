<template>
  <div>
    <PageTitle title='Database' />
    <SearchBar />
    <SideBar />
  </div>
</template>

<script>
import SearchBar from '~/components/SearchBar.vue'
import SideBar from '~/components/SideBar.vue'
import PageTitle from '~/components/miscellaneous/page_title.vue'

export default {
  name: 'Database',

  components: {
      SearchBar,
      SideBar,
      PageTitle
  }
}
</script>


<style>
  body {
    margin: 0;
  }
</style>
