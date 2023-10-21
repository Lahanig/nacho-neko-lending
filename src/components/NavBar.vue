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
                {id: 1, name: 'Name card', href: '#name-card'},
                {id: 2, name: 'Gallery', href: '#gallery'},
                {id: 3, name: 'Trivia', href: '#trivia'}
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
        <nav class="shadow non-select">
            <div class="nav-item-logo">
                <img alt="logo" class="logo" src="/logo-2.png" width="60" height="60" />
                <span>Nacho Dayo</span>
            </div>

            <div class="container mx-auto tablet shadow p-0" style="justify-content: center; align-items: center; position: absolute; max-width: 100%;">
                <a v-for="tab in navTabs" :key="tab.id" :href="tab.href">
                    <div class="nav-item" draggable="false">
                        {{ tab.name }}
                    </div>
                </a>
            </div>

            <div class="container mx-auto desktop" style="justify-content: center; align-items: center; position: absolute; max-width: 100%;">
                <div class="nav-item" v-for="tab in navTabs" :key="tab.id">
                    <a :href="tab.href" draggable="false"> 
                        {{ tab.name }} 
                    </a>
                </div>
            </div>

            <div class="navbar-line">
                <button class="btn" @click="navbarMenu"><MenuOutline class="icon" /></button>
            </div>
        </nav>

        <div class="wrapper">
            <div class="wrapper-inner">
                
                <div class="container">

                    <div class="wrapper-inner-body my-auto">
                        <span>
                            The Nacho's Lending
                            This is a fan lending dedicated to Nacho Neko, it was created for the practice of website layout.
                            <button type="button" class="btn btn-primary mt-3" data-bs-toggle="modal" data-bs-target="#exampleModal">Fun alert</button>
                        </span>

                        
                    </div>

                </div>

            </div>
        </div>

        <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">Modal window</h1>
                        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Закрыть"></button>
                    </div>
                    <div class="modal-body">
                        This funy modal window
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped>
.wrapper {
    width: 100%;
    height: 100vh;

    margin-top: 75px;
}

.wrapper-inner {
    width: 100%;
    height: calc(100vh);

    display: flex;

    padding-top: calc(2rem + 10vh);

    background: url('../assets/imgs/background.png') no-repeat;
    background-position: 70%;
    background-size: cover;
    background-attachment: fixed;
}

.wrapper-inner-body {
    display: flex;
    flex-direction: column;

    width: 100%;

    border: 0px solid red;

    color: #eee;
}

.wrapper-inner-body span {
    display: flex;

    max-width: 450px;
    width: 100%;

    padding-left: 1rem;

    font-size: 1.6em;

    border: 0px solid red;

    flex-direction: column;
}

.wrapper-inner-body button {
    padding: 1rem;

    color: #eee;
    
    max-width: 150px;

    background-color: var(--primary-color);
    border-color: var(--primary-color);

    transition: all ease .3s;
}

.wrapper-inner-body button:hover {
    background-color: var(--primary-color-soft);
    border-color: var(--primary-color-soft);
}

.wrapper-inner-body button:focus {
    background-color: var(--primary-color-mute);
    border-color: var(--primary-color-mute);
}

nav {
  width: 100%;

  font-size: 12px;
  text-align: center;

  border: 0px solid red;

  display: flex;
  position: fixed;

  background-color: var(--color-background-mute)!important;

  z-index: 2;

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

    .wrapper-inner {
        background-position: top;
        padding-top: 12rem;
    }

    .wrapper-inner-body span {
        margin-left: 15%;

        font-size: 1.8em;
    }
}

@media (min-width: 2624px) {
    .wrapper-inner-body span {
        font-size: 2.4em;

        margin-left: 10%;

        max-width: 600px;
    }

    .wrapper-inner {
        padding-top: calc(12rem + 10vh);
    }
}
</style>