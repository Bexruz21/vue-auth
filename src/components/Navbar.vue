<script setup>
import { ref } from 'vue';
const showMenu = ref(false)
</script>
<template>
    <nav class="navbar">
        <div class="navbar__brand">
            <router-link to="/">Vue-Auth</router-link>
            <i class="fa-solid fa-bars navbar__burger" @click="showMenu = !showMenu"></i>
        </div>
        <div class="navbar__menu" :class="showMenu ? 'navbar__menu_open' : ''">
            <i class="fa-solid fa-x navbar__burger" @click="showMenu = !showMenu"></i>
            <router-link to="/login" class="navbar__login">Login</router-link>
            <router-link to="/sign-up" class="navbar__sign-up">Sign-up</router-link>
        </div>
    </nav>
</template>

<style scoped>
.navbar {
    width: 100%;
    height: 80px;
    padding: 0px 80px;
    background-color: #2c2c2c;
    display: flex;
    align-items: center;
}
.navbar__brand {
    flex: 1;
}
.navbar__brand a {
    color: white;
    font-size: 25px;
}
.navbar__menu {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: end;
    gap: 10px;
}
.navbar__menu a {
    color: white;
    font-size: larger;
    padding: 8px 12px;
    transition: .2s all;
}
.navbar__burger {
    display: none;
    font-weight: 900;
    font-size: 30px;
    color: white;
}
.navbar__menu .navbar__login:hover {
    text-shadow: 1px 1px 3px gainsboro;
}
.navbar__menu .navbar__sign-up {
    background-color: aliceblue;
    color: #1c1c1c !important;
    border-radius: 20px;
    padding: 8px 24px;
}
.navbar__menu .navbar__sign-up:hover {
    box-shadow: 1px 1px 3px gainsboro;
}
@media screen and (max-width:426px) {
    .navbar {
        padding: 0px 30px;
        position: relative;
    }
    .navbar__brand {
        display: flex;
        flex: 1;
        justify-content: space-between;
        align-items: center;
    }
    .navbar__burger {
        display: block;
    }
    .navbar__menu {
        position: absolute;
        right: 0;
        top: 0;
        z-index: 1;
        width: 70%;
        height: 100vh;
        flex-direction: column;
        justify-content: start;
        background-color: #2a2a2a;
        box-shadow: 0px 0px 3px gainsboro;
        padding: 20px;
        transition: .3s all;
        transform: translateX(100%);
    }
    .navbar__sign-up {
        width: 100%;
        text-align: center;
    }
    .navbar__menu .navbar__burger {
        align-self: flex-end;
    }
    .navbar__menu_open {
        transform: translateX(0%);
    }
}
</style>