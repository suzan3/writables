<template>
<q-layout view="lHh Lpr lFf">
    <q-header elevated>
        <q-toolbar>

            <q-btn class="sm-show" dense flat round icon="menu" @click="left = !left" />

            <q-toolbar-title>
                <img src="~assets/logo.png" class="q-ma-sm" width="30px" alt="">
            </q-toolbar-title>
            <div class="lg-show">
                <div class="nav-link">HOME</div>
                <div class="nav-link">
                    <router-link to="/services">SERVICES</router-link>
                </div>
                <div class="nav-link">LIBRARY</div>
                <div class="nav-link">
                    <router-link to="/platforms">PLATFORMS</router-link>
                </div>
                <q-btn outline style="color: goldenrod;" label="LOG IN/ SIGN UP" />
                <div class="nav-link">EN/AR</div>

            </div>
        </q-toolbar>
    </q-header>
    <q-drawer behavior="mobile" show-if-above v-model="left" side="left" bordered>
        <div class="nav-link">HOME</div>
        <div class="nav-link">
            <router-link to="/services">SERVICES</router-link>
        </div>
        <div class="nav-link">LIBRARY</div>
        <div class="nav-link">
            <router-link to="/platforms">PLATFORMS</router-link>
        </div>
        <q-btn class="nav-link" outline style="color: goldenrod;" label="LOG IN/ SIGN UP" />
        <div class="nav-link">EN/AR</div>
    </q-drawer>

    <div class="bg">
        <q-page-container>
            <router-view />
        </q-page-container>
        <theFooter></theFooter>
    </div>
</q-layout>
</template>

<style lang="scss">
.sm-show {
    display: none;
}
.bg {
    background-image: url('~assets/left-bg.jpg') , url('~assets/right-bg.jpg');
    background-repeat: no-repeat,no-repeat;
    background-position: right center,left center;
}
@media only screen and (max-width: 775px) {
    .sm-show {
        display: block !important;
    }

    .nav-link {
        padding: 1rem;
    }

    .q-drawer__content {
        background-color: #EDEEEF;
    }

    .lg-show {
        display: none !important;
    }
}

.lg-show {
    display: contents;
}

.q-layout__section--marginal {
    background-color: #EDEEEF !important;
}

.q-layout__shadow:after {
    box-shadow: none !important;
}

.nav-link {
    color: black;
    font-family: 'AGENCYR';
    font-size: 20px;
    cursor: pointer;
    margin-right: 10px;
    margin-left: 10px;

    a {
        color: black !important;
        text-decoration: none !important;
    }

    a.router-link-exact-active,
    a.router-link-active {
        color: #BC8037 !important;
        font-weight: bold;
    }
}
</style>

<script>
import EssentialLink from 'components/EssentialLink.vue';
import theFooter from 'pages/theFooter.vue';
const linksData = [{
        title: 'Docs',
        caption: 'quasar.dev',
        icon: 'school',
        link: 'https://quasar.dev'
    },
    {
        title: 'Github',
        caption: 'github.com/quasarframework',
        icon: 'code',
        link: 'https://github.com/quasarframework'
    },
    {
        title: 'Discord Chat Channel',
        caption: 'chat.quasar.dev',
        icon: 'chat',
        link: 'https://chat.quasar.dev'
    },
    {
        title: 'Forum',
        caption: 'forum.quasar.dev',
        icon: 'record_voice_over',
        link: 'https://forum.quasar.dev'
    },
    {
        title: 'Twitter',
        caption: '@quasarframework',
        icon: 'rss_feed',
        link: 'https://twitter.quasar.dev'
    },
    {
        title: 'Facebook',
        caption: '@QuasarFramework',
        icon: 'public',
        link: 'https://facebook.quasar.dev'
    },
    {
        title: 'Quasar Awesome',
        caption: 'Community Quasar projects',
        icon: 'favorite',
        link: 'https://awesome.quasar.dev'
    }
];

export default {
    name: 'MainLayout',
    components: {
        theFooter
    },
    // components: { EssentialLink },
    data() {
        return {
            leftDrawerOpen: false,
            essentialLinks: linksData,
            left: false
        }
    }
}
</script>
