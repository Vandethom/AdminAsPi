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
      <label for='content'>
        Contenu
      <textarea
			name='content'
			id='content'
			v-model='course_preview.content'
			v-on:input='preview(course_preview.content)'
			/>
      </label>
  </form>
</template>

<script>
export default {
    name: 'CreateCourseForm',

    data() {
      return {
        course_preview: {
			content: null,
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
        width: 45vw;
        display: flex;
        flex-direction: column;

        label {
			display: grid;
			grid-template-columns: 105px 175px;
			padding: 5px;
			font-family: 'Vollkorn';
			color: #efefef;
			width: 40px;
			height: 32px;
        }

        input {
          	justify-self: center;
        }

        #content {
			width: 40vw;
			height: 40vh;
        }
    }
</style>