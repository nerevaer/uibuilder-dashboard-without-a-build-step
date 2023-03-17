<template>
    <div class="dashboard">
        <!--<router-view></router-view>-->
        <Sidebar></Sidebar>
        <div class="content">
            <router-view></router-view>
            <!--<router-view name="Sidebar"></router-view>-->
        </div>
    </div>
</template>

<script>
const Sidebar = httpVueLoader('../components/Sidebar.vue');
const Messages = httpVueLoader('./Messages.vue');
const Overview = httpVueLoader('./Overview.vue');
/*const routeDefs = [{
        path: '',
        component: Sidebar,
        children: [{
            path: '/',
            components: Overview,
          },{
            path: '/messages',
            components: Messages,
}]}]*/
const routeDefs = [
    {
        path: '/',
        component: Sidebar
    },
    {
        path: '/overview',
        component: Overview
    },{
        path: '/messages',
        component: Messages
    }
]
module.exports = {
    /** Allow greeting and who to be passed as parameters but provide defaults
     * @see https://vuejs.org/v2/guide/components-props.html#Prop-Validation
     */
    router: new VueRouter({routes: routeDefs}),
    components: {
        'Sidebar': Sidebar,
        'Overview': Overview,
        'Messages': Messages
    }
}
</script>

<style>
.dashboard {
    display: grid;
    grid-template-columns: 1fr 5fr;
    background-color: rgba(17, 10, 82, 0.719);
    height: 100vh;
    width: 100vw;
}
.content {
    background-color: white;
    border-radius: 5px;
    margin: 6px 6px 6px 0px;
}
</style>