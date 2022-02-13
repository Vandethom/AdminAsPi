<template>
  <form class="create_course_form" action="">
      <label for="title">
        Titre
        <input
          id='preview_title'
          type='text' name='title'
          v-on:input='preview(course_preview.title)'
          v-model='course_preview.title'
          >
      </label>
      <label for="level">
        Niveau
        <input
          list='level'
          name='level'
          v-on:input='preview(course_preview.level)'
          v-model='course_preview.level'
          >
        <datalist id='level'>
          <option value='6e' />
          <option value='5e' />
          <option value='4e' />
          <option value='3e' />
        </datalist>
      </label>
      <label for='theme'>
        Thème
        <input
          list='theme'
          v-on:input='preview(course_preview.theme)'
          v-model='course_preview.theme'
          >
        <datalist id='theme'>
            <option value='Data' />
            <option value='Arithmétique' />
            <option value='Géométrie' />
            <option value='Fonctions' />
        </datalist>
      </label>
  </form>
</template>

<script>
export default {
    name: 'CreateCourseForm',

    data() {
      return {
        course_preview: {
          level: null,
          theme: null,
          title: null
        }
      }
    },

    methods: {
      preview(content) {
        console.log(content)
        console.log(this.course_preview)
        this.$emit('updatepreview', this.course_preview)
      }
    }
}
</script>

<style lang='scss'>
    .create_course_form {
        width: 260px;
        display: flex;
        flex-direction: column;

        label {
            text-align: right;
            color: #efefef;
            font-family: 'Vollkorn';
            font-size: 15px;
        }
        input {
            height: 24px;
            width: 180px;
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            color: #121212;
            background: #efefef;
            margin: 6px;
        }
    }
</style>