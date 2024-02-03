<script setup>

</script>
<template>
    <nav class="navbar">
        <div class="navbar__brand">
            <router-link to="/">Vue-Auth</router-link>
            <i class="fa-solid fa-bars navbar__burger"></i>
        </div>
        <div class="navbar__menu">
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
        padding: 0px 40px;
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
        display: none;
    }
}
</style>