<template>
    <b-navbar class="navbar" centered type="is-primary">
        <template #brand>
            <b-navbar-item tag="router-link" :to="{ path: '/' }">
                <img class="navbar__img" src="@/assets/images/eric-flores-logo.png" alt="My Logo">
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-item class="navbar__link" v-for="(item, index) in navbarItems" :key="'navbar-item-' + index"
                :href="item.to">
                {{ item.title }}
            </b-navbar-item>
        </template>
    </b-navbar>
</template>
<script>
export default {
    name: 'NavbarComponent',
    data: () => ({
        navbarItems: [
            {
                title: 'Home',
                to: '/#home',
            },
            {
                title: 'About',
                to: { name: 'index' },
            },
            {
                title: 'Skills',
                to: { name: 'index' },
            },
            {
                title: 'Work',
                to: { name: 'index' },
            },
            {
                title: 'Contact',
                to: { name: 'index' },
            },
        ]
    })
}
</script>
<style lang="scss" scoped>
.navbar {
    min-height: 56px;

    &__link {
        font-size: 2rem;
        padding-left: 2rem;
        padding-right: 2rem;
    }

}
</style>