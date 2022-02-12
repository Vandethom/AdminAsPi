<template>
    <div class="side_bar">
        <p id='logo'>π</p>
        <ul>
            <a href='/' id='side_menu_home'>
                <img src='@/assets/images/home.png' alt="Home icon">
                <p>Accueil</p>
            </a>
            <a href='/' id='side_menu_dashboard'>
                <img src='@/assets/images/dashboard.png' alt="Dashboard icon">
                <p>Dashboard</p>
            </a>
            <a href='/database' id='side_menu_database'>
                <img src='@/assets/images/database.png' alt="database icon">
                <p>Database</p>
            </a>
            <a href='/' id='side_menu_settings'>
                <img src='@/assets/images/settings.png' alt="settings icon">
                <p>Paramètres</p>
            </a>
            <a href='/' id='side_menu_disconnect'>
                <img src='@/assets/images/disconnect.png' alt="log off icon">
                <p>Déconnexion</p>
            </a>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'SideBar'

}
</script>

<style lang='scss'>
    .side_bar {
        background-color: #072E5B;
        width: 225px;
        height: 100vh;

        #logo {
            padding-top: 4vh;
            margin: 0 0 12vh 35%;
            font-size: 80px;
            font-family: 'Vollkorn';
            color: #FAE3B4;
        }

        a {
            display: flex;
            cursor: pointer;
            align-items: center;
            font-size: 18px;
            font-family: 'Vollkorn';
            text-decoration: none;
            color: #efefef;
            margin-bottom: 10px;
            
            img {
                width: 55px;
                height: 55px;
                margin-right: 12px;
            }
        }

        #side_menu_disconnect {
            margin-top: 7.5vh;
        }
    }
</style>