<template>
    <section class="course_preview">
        <h2>Prévisualisation</h2>
        <HorizontalRule />
        <article class='rendering_preview'>
            <h3 class='preview_title'>{{ title }}</h3>
            <p class='preview_level'>{{ level }}</p>
            <p class='preview_theme'>{{ theme }}</p>
            <p class='preview_content'>{{ content }}</p>
        </article>
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
        content: String,
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

        .rendering_preview {
            display: flex;
            height: 92vh;
            flex-direction: column;
            margin-left: 16px;
            
            .preview_title {
                align-self: center;
                font-family: 'Vollkorn';
            }

            .preview_level {
                transform: translate(450px, -80px);
            }

            .preview_theme {
                transform: translate(420px, -110px)
            }

            .preview_content {
                overflow: scroll;
                white-space: pre-wrap;
                padding: 12px;
                transform: translateY(-75px);
            }
        }   
    }
</style>
