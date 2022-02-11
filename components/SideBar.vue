<template>
    <div class="side_bar">
        <p id='logo'>π</p>
        <ul>
            <div id='side_menu_home'>
                <img src='@/assets/images/home.png' alt="Home icon">
                <p>Accueil</p>
            </div>
            <div id='side_menu_dashboard'>
                <img src='@/assets/images/dashboard.png' alt="Dashboard icon">
                <p>Dashboard</p>
            </div>
            <div id='side_menu_database'>
                <img src='@/assets/images/database.png' alt="database icon">
                <p>Database</p>
            </div>
            <div id='side_menu_settings'>
                <img src='@/assets/images/settings.png' alt="settings icon">
                <p>Paramètres</p>
            </div>
            <div id='side_menu_disconnect'>
                <img src='@/assets/images/disconnect.png' alt="log off icon">
                <p>Déconnexion</p>
            </div>
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
            margin: 0 auto;
            font-size: 80px;
            font-family: 'Vollkorn';
            color: #FAE3B4;
        }

        div {
            margin-top: 40px;
            display: flex;
            align-items: center;
            font-size: 18px;
            font-family: 'Vollkorn';
            color: #efefef;
            
            img {
                width: 50px;
                height: 50px;
                margin-right: 12px;
            }
        }
    }
</style>