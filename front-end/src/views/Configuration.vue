<template lang="html">
    <div class="container-scroller">
        <app-header></app-header>
        <div class="container-fluid page-body-wrapper">
            <app-sidebar></app-sidebar>
            <div class="main-panel">
                <div class="content-wrapper">
                    <section class="dashboard">
                        <app-conf-tabs></app-conf-tabs>
                    </section>
                </div>
                <app-footer></app-footer>
            </div>
        </div>
    </div>
</template>

<script  lang="js">
    // @ is an alias to /src
    import AppHeader from '@/components/AppHeader'
    import AppSidebar from '@/components/AppSidebar'
    import AppFooter from '@/components/AppFooter'
    import AppConfTabs from '@/components/AppConfTabs'

    export default {
        name: "configuration",
        components: {
            AppHeader,
            AppSidebar,
            AppFooter,
            AppConfTabs
        }
    }
</script>

<style scoped>

</style>