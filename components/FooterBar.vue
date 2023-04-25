<template>
    <footer class="footer">
        <div class="content has-text-centered">
            <div class="footer__links columns">
                <div class="column" v-for="link in links" :key="link.icon">
                    <a :href="link.url" target="_blank">
                        <b-icon :icon="link.icon" :size="link.iconSize" :type="link.type">
                        </b-icon>
                    </a>
                </div>
            </div>
            <div>
                <p class="footer__text">
                    Created by <strong>Eric Flores</strong> <br />
                    Inspired by the videogame series Watchdogs
                </p>
                <span>© {{ currentYear }} Eric Flores</span>
            </div>
        </div>
    </footer>
</template>
<script>
export default {
    name: 'FooterBarComponent',
    data: () => ({
        links: [
            {
                icon: "linkedin",
                iconSize: 'is-large',
                url: "https://www.linkedin.com/in/eric-joseph-flores-b3a36a153",
                type: "is-white"
            },
            {
                icon: "github",
                iconSize: 'is-large',
                url: "https://github.com/AgentProxy",
                type: "is-white"
            },
            {
                icon: "gitlab",
                iconSize: 'is-large',
                url: "https://gitlab.com/AgentProxy",
                type: "is-white"
            },
            {
                icon: "email",
                iconSize: 'is-large',
                url: "mailto:ericjoseph.flores1@gmail.com",
                type: "is-white"
            },
        ]
    }),
    computed: {
        currentYear() {
            return new Date().getFullYear();
        }
    }
}
</script>
<style lang="scss" scoped>
.footer {
    &__links {
        margin-left: auto;
        margin-right: auto;
        max-width: 300px;
    }

    &__text {
        color: white;
        font-size: 20px;
    }
}
</style>