<!-- eslint-disable vue/no-unused-components -->
<script>
import { RouterLink } from 'vue-router'
import { MenuOutline } from '@vicons/ionicons5'
import { ref } from 'vue'

export default {
    components: {
        RouterLink,
        MenuOutline
    },
    data() {
        return {
            isMenuShow: ref(false),
            navTabs: ref([
                {id: 0, name: 'Home', href: '#'},
                {id: 1, name: 'About', href: '#about'},
                {id: 2, name: 'Trivia', href: '#trivia'}
            ])
        }
    },
    methods: {
        navbarMenu() {
            const menu = document.querySelector('.tablet')

            if (this.isMenuShow === false) {
                menu.style.display = 'block'
                this.isMenuShow = true
            } else {
                menu.style.display = 'none'
                this.isMenuShow = false
            }
        }
    }
}
</script>

<template>
    <header>
        <nav class="shadow">
            <div class="nav-item-logo">
                <img alt="logo" class="logo" src="/logo-2.png" width="60" height="60" />
                <span>Nacho Dayo</span>
            </div>

            <div class="container mx-auto tablet shadow p-0" style="justify-content: center; align-items: center; position: absolute; max-width: 100%;">
                <a v-for="tab in navTabs" :key="tab.id" :href="tab.href" >
                    <div class="nav-item">
                        {{ tab.name }}
                    </div>
                </a>
            </div>

            <div class="container mx-auto desktop" style="justify-content: center; align-items: center; position: absolute; max-width: 100%;">
                <div class="nav-item" v-for="tab in navTabs" :key="tab.id">
                    <a :href="tab.href"> 
                        {{ tab.name }} 
                    </a>
                </div>
            </div>

            <div class="navbar-line">
                <button class="btn" @click="navbarMenu"><MenuOutline class="icon" /></button>
            </div>
        </nav>

        <div class="wrapper">
        </div>
    </header>
</template>

<style scoped>
header {
    margin-bottom: 5rem;
}

nav {
  width: 100%;

  font-size: 12px;
  text-align: center;

  border: 0px solid red;

  display: flex;
  position: fixed;

  background-color: var(--color-background-mute)!important;

  z-index: 1;

  top: 0;
}

.nav-item {
    padding: 1rem 0rem;

    font-size: 1.5em;

    color: var(--color-text)!important;
}

.nav-item a {
    color: var(--color-text)!important;
}

.navbar-line {
    width: 50%;

    opacity: 1;

    margin-left: auto;

    background-color: var(--primary-color);

    border-radius: 0 0 0 100px;

    display: flex;
    align-items: center;

    justify-content: end;
}

.navbar-line .btn {
    padding: .5rem .5rem;
    margin-right: .5rem;
}

.navbar-line .btn .icon {
    width: 50px;
    border: none;
}

.navbar-line .btn .icon:focus {
    border: none;
}

.logo {
    display: flex;
}

.nav-item-logo {
    position: relative;
    display: flex;

    margin: .5rem 1rem; 
    
    align-items: center;
}

.nav-item-logo span {
    margin: 0rem 1rem; 
    font-size: 1.5em;

    display: block;
}

.tablet {
    margin: 4.7812rem;

    display: none;
    
    z-index: 1;

    background-color: var(--color-background);
}

.desktop {
    display: none;
}

header {
  line-height: 1.5;
  max-height: 100vh;

  background-color: var(--color-background)!important;
}

@media (min-width: 1024px) {
    .tablet {
        display: none!important;
    }

    .desktop {
        display: flex;
    }

    .nav-item {
        padding: 1.5rem 1rem;
    }

    .navbar-line .btn {
        display: none;
    }
}
</style>