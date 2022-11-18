<template>
    <div class="navbar">
        <div class="sidebar-logo">
            <div id="mySidenav" class="sidenav">
                <h1>
                    <span class="google blue">G</span>
                    <span class="google red">o</span>
                    <span class="google yellow">o</span>
                    <span class="google blue">g</span>
                    <span class="google green">l</span>
                    <span class="google red">e</span>
                    <span class="translate"> Translate</span>
                    <a href="javascript:void(0)" class="closebtn" v-on:click="closeNav()">&times;</a>
                </h1>
                <a class="navlink about" href="#">About Google Translator</a>
                <a class="navlink" href="#">Services</a>
                <a class="navlink" href="#">Clients</a>
                <a class="navlink" href="#">Contact</a>
            </div>
            <span class="openbtn" v-on:click="openNav()">&#9776;</span>
            <h1>
                <span class="google blue">G</span>
                <span class="google red">o</span>
                <span class="google yellow">o</span>
                <span class="google blue">g</span>
                <span class="google green">l</span>
                <span class="google red">e</span>
                <span class="translate"> Translate</span>
            </h1>
        </div>
        <div class="app-navbar-access">
            <div class="dropdown">
                <button class="dropbtn"><img src="../assets/352018_apps_icon.png"/></button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
            <button class="sign-up">Sign Up</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NavigationBar',
    methods: {
        openNav() {
            document.getElementById("mySidenav").style.width = "250px";
        },
        closeNav() {
            document.getElementById("mySidenav").style.width = "0";
        }
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');

.navbar {
    height: 60px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #bbb;
}

.sidebar-logo {
    display: flex;
    width: 250px;
    justify-content: space-around;
    align-items: center;
}

.app-navbar-access {
    margin: 0 8px 0 0;
    display: flex;
    width: 160px;
    justify-content: space-around;
    align-items: center;
}

.sidenav {
    border-right: 1px solid #ccc;
    margin: 0 auto 0;
    height: 100%;
    width: 0;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    overflow-x: hidden;
    transition: 0.5s;
    padding-top: 8px;
    background-color: white;
}

.navlink {
    color: black;
    padding: 24px 8px 24px 32px;
    text-decoration: none;
    text-align: left;
    font-size: 14px;
    display: block;
    transition: 0.3s;
}

.navlink.about {
    text-decoration: underline;
    border-bottom: 1px solid #ccc;
}

.sidenav a:hover {
    background-color: #ddd;
}

.closebtn {
    position: absolute;
    top: 0;
    right: 25px;
    font-size: 16px;
    margin-top: 16px;
    margin-left: 50px;
    padding: 0;
    text-decoration: none;
}

.openbtn {
    opacity: 0.8;
    font-size:24px;
    cursor:pointer
}

.google, .translate {
    font-family: 'Open Sans', sans-serif;
    letter-spacing: 3;
}

.translate {
    font-size: 20px;
    color: #5f6368;
}

.google.red {
    color: red;
}

.google.blue {
    color: #1a73e8;;
}

.google.green {
    color: greenyellow;
}

.google.yellow {
    color: gold;
}

.dropbtn {
    background-color: #fff;
    padding: 8px;
    border: none;
}

.dropbtn img {
    opacity: 0.6;
    width: 24px;
    height: auto;
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f1f1f1;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {background-color: #ddd;}

.dropdown:hover .dropdown-content {display: block;}

.dropdown:hover .dropbtn {background-color: #bbb;}

.sign-up {
    font-family: Google Sans,Roboto,Helvetica,Arial,sans-serif;
    font-weight: 500;
    border: none;
    border-radius: 4px;
    width: 96px;
    color: #fff;
    padding: 9px 23px;
    background-color: #1a73e8;
}

</style>