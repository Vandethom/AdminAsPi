<template>
  <div>
    <SearchBar />
    <div class="main_container">
      <SideBar />
      <section class='main_section'>
        <PageTitle page_title='Création de document' />
        <section class="editor_icons">
            <div>
                <AddTextIcon />
                <p class='icon_legend'>Zone de texte</p>
            </div>
            <span class='vertical_line' />
            <div>
                <CommentIcon />
                <p class='icon_legend'>Commentaire</p>
            </div>
            <span class='vertical_line' />
            <div>
                <FormulaIcon />
                <p class='icon_legend'>Notation</p>
            </div>
            <span class='vertical_line' />
            <div>
                <DefinitionIcon />
                <p class='icon_legend'>Définition</p>
            </div>
        </section>
        <HorizontalRule />
        <CreateCourseForm @updatepreview='update_preview($event)' />
      </section>
      <CoursePreview
        :title='this.preview.title'
        :level='this.preview.level'
        :theme='this.preview.theme'
        :content='this.preview.content'
      />
    </div>
  </div>
</template>

<script>
import AddTextIcon from '~/assets/icons/addText.vue'
import Card from '~/components/Card.vue'
import CommentIcon from '~/assets/icons/comment.vue'
import CoursePreview from '~/components/course_preview.vue'
import CreateCourseForm from '~/components/create_course_form.vue'
import CreateCourseIcon from '~/assets/icons/create_course.vue'
import DefinitionIcon from '~/assets/icons/definition.vue'
import FormulaIcon from '~/assets/icons/formula.vue'
import HorizontalRule from '~/components/miscellaneous/hr.vue'
import PageTitle from '~/components/miscellaneous/page_title.vue'
import SearchBar from '~/components/SearchBar.vue'
import SideBar from '~/components/SideBar.vue'

export default {
  name: 'Database',

  components: {
      AddTextIcon,
      Card,
      CommentIcon,
      CoursePreview,
      CreateCourseForm,
      CreateCourseIcon,
      DefinitionIcon,
      FormulaIcon,
      HorizontalRule,
      PageTitle,
      SearchBar,
      SideBar
  },

  data() {
    return {
      preview: {}
    }
  },
  
  methods: {
    update_preview(event) {
      this.preview = event
      console.log('from parent :::', this.preview)
    }
  }
}
</script>


<style lang='scss'>
  body {
    margin: 0;
  }

  .main_container {
    display: flex;

    .main_section {
        display: flex;
        flex-direction: column;
        //align-items: center;
        margin: 100px 0 60px 5vw;

        .editor_icons {
            display: flex;
            justify-content: center;
            width: 650px;
            height: 105px;
            padding: 16px;
            border-radius: 4px;
            background-color: #194d88;
            cursor: pointer;

            div {
              margin: 0 42px;

              svg {
                  width: 65px;
                  height: 65px;
              }
            }

            .vertical_line {
              border-left: 1px solid #FAE3B4;
              height: 85px;
            }

            .icon_legend {
                font-size: 14px;
                font-family: 'Vollkorn';
                color: #efefef;
            }
        }
    }
  }
</style>
