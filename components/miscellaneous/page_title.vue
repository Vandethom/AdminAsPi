<template>
  <h1>{{ title }}</h1>
</template>

<script>
export default {
    name: 'PageTitle',

    'props': {
        title: {
            type: String
        }
    }
}
</script>

<style>
    h1 {
        position: relative;
        top: 65px;
        left: 275px;
        margin: 0;
        font-size: 30px;
        color: #efefef;
    }
</style>