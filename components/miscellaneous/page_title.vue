<template>
  <h1 id='page_title'>{{ page_title }}</h1>
</template>

<script>
export default {
    name: 'PageTitle',

    'props': {
        page_title: String
    }
}
</script>

<style lang='scss'>
    h1 {
        margin: 3.5vh -7vw;
        font-size: 30px;
        color: #efefef;
    }
</style>