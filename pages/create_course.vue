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
            <div>
                <CommentIcon />
                <p class='icon_legend'>Commentaire</p>
            </div>
            <div>
                <FormulaIcon />
                <p class='icon_legend'>Notation</p>
            </div>
            <div>
                <DefinitionIcon />
                <p class='icon_legend'>Définition</p>
            </div>
        </section>
        <hr />
      </section>
    </div>
  </div>
</template>

<script>
import Card from '~/components/Card.vue'
import AddTextIcon from '~/assets/icons/addText.vue'
import CommentIcon from '~/assets/icons/comment.vue'
import CreateCourseIcon from '~/assets/icons/create_course.vue'
import DefinitionIcon from '~/assets/icons/definition.vue'
import FormulaIcon from '~/assets/icons/formula.vue'
import PageTitle from '~/components/miscellaneous/page_title.vue'
import SearchBar from '~/components/SearchBar.vue'
import SideBar from '~/components/SideBar.vue'

export default {
  name: 'Database',

  components: {
      AddTextIcon,
      Card,
      CommentIcon,
      CreateCourseIcon,
      DefinitionIcon,
      FormulaIcon,
      PageTitle,
      SearchBar,
      SideBar
  }
}
</script>


<style lang='scss'>
  body {
    margin: 0;
  }

  .main_container {
    display: flex;

    hr {
      width: 55vw;
      margin: 45px auto;
      border-top: 1px solid #FAE3B4;
      filter: drop-shadow(0 2px 12px #FAE3B4);
    }

    .main_section {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 45px 0 60px 10vw;

        .editor_icons {
            display: flex;
            justify-content: center;
            width: 800px;
            height: 105px;
            padding: 16px;
            border-radius: 4px;
            background-color: #194d88;
            cursor: pointer;

            svg {
                width: 65px;
                height: 65px;
                margin-right: 84px;
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
