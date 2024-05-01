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
            <div class="fourth-section__content">
                <p class="title">We Are The Right Fit For Those Who Are Searching For...</p>
                <div class="grid">
                    <div class="grid-item" v-for="x in cardContent" :key="x.number" >
                        <CardNumbered :number="x.number"  :title="x.title" :content="x.content"/>
                    </div>
                </div>
            </div>
        </section>

        <section class="fifth-section">
            <div class="fifth-section__content">
                <p class="title">Explore our studios</p>
                <div class="grid">
                    <div class="grid-item" v-for="x in studios" :key="x.name">
                        <Studio :image="x.image" :name="x.name" :location="x.location"/>
                    </div>
                </div>
            </div>
        </section>

    </div>
    
</template>


<script setup>
    import Menu from './components/Menu.vue'
    import Navbar from './components/Navbar.vue'
    import ImageSlider from './components/ImageSlider.vue'
    import CardNumbered from './components/CardNumbered.vue'
    import Studio from './components/Studio.vue'

    import './assets/styles.scss'

    import { ref, computed, onMounted } from 'vue'

    const menuState = ref('inactive-menu')

    function openMenu() {
        menuState.value = 'active-menu' 
    }
    function closeMenu() {
        menuState.value = 'inactive-menu' 
    }

    const cardContent = [
        {
            'number': '01',
            'title': 'HOLISTIC APPROACH\nTO PERSONAL TRAINING',
            'content':'We are committed to keeping you accountable with the high care and high-challenge method that seeks to understand, empower and synergise with you on your journey to your breakthrough. We understand that the journey is not going to be easy but we also know that each one has what it takes to overcome, therefore, it is our goal to guide you toward doing that. The right coach and environment can help you erase limitations and realise your potential. But only if it’s the right coach and environment.'
        },
        {
            'number': '02',
            'title': 'HIGH CARE \n& HIGH CHALLENGE',
            'content':'We are committed to keeping you accountable with the high care and high-challenge method that seeks to understand, empower and synergise with you on your journey to your breakthrough.\nWe understand that the journey is not going to be easy but we also know that each one has what it takes to overcome, therefore, it is our goal to guide you toward doing that. The right coach and environment can help you erase limitations and realise your potential. But only if it’s the right coach and environment.'
        },{
            'number': '03',
            'title': 'EMPOWERING\nPRIVATE SPACE',
            'content':'Crowded workout spaces and awkward stares from others are things in the past.\nYou deserve a 5-star rated personal training experience from the moment you walk in, to the moment you walk out - clean, sanitized, judgment-free and empowering. Our appointment based business model will mean that there will be no gym members loitering around which could be off putting for some. What you will get instead is an environment where everyone is focused on what\'s in front of them with their respective coach.'
        },
    ]

    const studios = [
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Kota Laksamana',
            'location': 'Melaka',
        },
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Montkiara',
            'location': 'Kuala Lumpur',
        },
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Ayer Keroh',
            'location': 'Melaka',
        },
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Damansara Heights',
            'location': 'Kuala Lumpur',
        },
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Bukit Jalil',
            'location': 'Kuala Lumpur',
        },
        {
            'image': 'https://placehold.co/1200x800',
            'name': 'Jalan Ampang',
            'location': 'Kuala Lumpur',
        },
    ]
</script>



