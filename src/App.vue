<template>
    <div class="body">
        <Menu :menuState="menuState" @closeMenu="closeMenu"/>

        <section class="first-section">
            <Navbar :menuState="menuState" @openMenu="openMenu" :mainMenu="1"/>
            <h1>Personal Training Redefined for Holistic Living</h1>
        </section>

        <section class="second-section">
            <div class="grid">
                <div class="grid-item">
                    <p class="title">MOVE into your new self.</p>
                </div>
                <div class="grid-item description">
                    <p>If you are looking for a personal trainer to help you, you’re in the right place at the right moment because you know…</p>
                    <p>You want to attain a fit and healthy lifestyle without feeling stuck, disheartened, and lost.</p>
                    <p>You struggle with consistency and enjoyment in trying to live a healthier lifestyle because you can’t see how your efforts pay off or lead you to the next thing.</p>
                    <p>You’re tired of only getting ONE piece of the puzzle of how to get towards your fitness goal and guessing what works for your unique lifestyle.</p>
                    <p>What if you could have a proven roadmap that permanently shifts you towards greater health, movement, and fitness?</p>
                </div>
            </div>
        </section>

        <section class="third-section">
            <div class="flex">
                <ImageSlider />
                <div class="flex-content content">
                    <div class="box">
                        <div class="box-content">
                            <p class="title">PERSONALISED BREAKTHROUGH JOURNEY</p>
                            <p>We believe in training bodies and minds whilst having breakthroughs along the path to our destiny. Our personal training method and roadmaps are designed to understand and adapt to your unique needs, and our personal trainers are empowered to provide high care and high challenge for you to thrive. Everything we do at MOVE carries our mission to enable and empower people to move well and live more.</p>
                            <button class="main-button">Book a FREE Consultation</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="fourth-section">
        </section>

    </div>
    
</template>


<script setup>
    import Menu from './components/Menu.vue'
    import Navbar from './components/Navbar.vue'
    import ImageSlider from './components/ImageSlider.vue'

    import './assets/styles.scss'

    import { ref, computed, onMounted } from 'vue'

    const menuState = ref('inactive-menu')

    function openMenu() {
        menuState.value = 'active-menu' 
    }
    function closeMenu() {
        menuState.value = 'inactive-menu' 
    }
</script>



