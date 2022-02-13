<template>
  <div>
    <SearchBar />
    <div class="main_container">
      <SideBar />
      <section class='main_section'>
        <PageTitle page_title='Database' />
        <Nuxt-Link to='/create_course' class='create_course_button'>
          <CreateCourseIcon />
          <p>Ajouter un contenu</p>
        </Nuxt-Link>
        <section class="card_container">
          <Card
            card_title='Nouveaux Cours'
            card_data=8
            card_legend='créés cette dernière semaine'
            />
          <Card
            card_title='Nouveaux Exercices'
            card_data=11
            card_legend='créés cette dernière semaine'
            />
          <Card
            card_title='Corrections'
            card_data=47
            card_legend='en attente depuis une semaine'
            />
        </section>
        <hr />
      </section>
    </div>
  </div>
</template>

<script>
import Card from '~/components/Card.vue'
import CreateCourseIcon from '~/assets/icons/create_course.vue'
import PageTitle from '~/components/miscellaneous/page_title.vue'
import SearchBar from '~/components/SearchBar.vue'
import SideBar from '~/components/SideBar.vue'

export default {
  name: 'Database',

  components: {
      Card,
      CreateCourseIcon,
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

    .card_container {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      margin-left: 45px;
    }

    .main_section {
        margin: 45px 0 60px 10vw;

        .create_course_button {
          position: absolute;
          left: 85vw;
          top: 72px;
          display: flex;
          width: 180px;
          height: 65px;
          text-decoration: none;
          background-color: #494641;
          color: #20FBAC;
          font-size: 15px;
          font-family: 'Vollkorn';
          align-items: center;
          padding: 4px;
          border-radius: 4px;
          border: 1px solid #FAE3B4;

          svg {
            margin: 0 10px;
          }
        }
    }
  }
</style>
