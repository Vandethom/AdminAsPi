<template>
    <section class="course_preview">
        <h2>Prévisualisation</h2>
        <HorizontalRule />
        <h3>{{ title }}</h3>
        <p>{{ level }}</p>
        <p>{{ theme }}</p>
    </section>
</template>

<script>
import HorizontalRule from '~/components/miscellaneous/hr.vue'

export default {
    name: 'CoursePreview',

    components: {
        HorizontalRule
    },

    props: {
        level: String,
        theme: String,
        title: String
    }
}
</script>

<style lang='scss'>
    .course_preview {
        position: absolute;
        top: 45px;
        right: 0;
        top: 45px; // height of header : need to rearrange properly
        width: 28vw;
        height: 100vh;
        background-color: #121212;
        border: 1px solid #FAE3B4;
        border-radius: 2px;
        color: #efefef;

        h2 {
            color: #efefef;
            font-family: 'Vollkorn';
            margin-left: 16px;
        }
    }
</style>
