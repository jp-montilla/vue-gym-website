<template>
    <div class="navbar" >
        <nav :class="mainMenu == 1 ? 'nav-white' : 'nav-black'">
            <div class="navbar-brand">
                <img :src="mainMenu == 1 ? 'https://cdn.statically.io/img/www.moveprivatefitness.com/wp-content/uploads/2023/04/move-logo-black.png?quality=100&f=auto' : 'https://www.moveprivatefitness.com/wp-content/uploads/2023/04/move-logo-white-1024x211.png'" alt="">
            </div>
            <div class="nav-group" :class="mainMenu == 1 ? 'nav-long' : 'nav-short'">
                <div>
                    <a href="#" class="nav-group__link">Studio <span><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M182.6 470.6c-12.5 12.5-32.8 12.5-45.3 0l-128-128c-9.2-9.2-11.9-22.9-6.9-34.9s16.6-19.8 29.6-19.8H288c12.9 0 24.6 7.8 29.6 19.8s2.2 25.7-6.9 34.9l-128 128z" :fill="mainMenu == 1 ? 'black' : 'white'"/></svg></span></a>
                </div>
                <button class="main-button">INQUIRE NOW</button>
                <svg v-if="mainMenu" @click="openMenu" class="nav__menu-button" xmlns="http://www.w3.org/2000/svg" width="247" viewBox="0 0 247 247" fill="none"><path d="M247 206H0V178.333H247V206ZM247 136.833H0V109.167H247V136.833ZM247 67.6667H123.5V40H247V67.6667Z" fill="black"></path></svg>
            </div>
        </nav>
    </div>
</template>


<script setup>
    import {defineProps} from 'vue'

    const emit = defineEmits(['openMenu'])

    const props = defineProps({
        menuState: {
            type: String,
            required: true,
        },
        mainMenu: {
            type: Number,
            required: true
        }
    });

    const openMenu = () => {
        emit('openMenu')
    }

</script>