<template>
    <div class="dashboard">
        <router-view></router-view>
            <!--<Sidebar/>-->   
        <div class="content">
            <router-view name="Sidebar"></router-view>
            
            <!--<router-view/>-->   
        </div>
    </div>
</template>






<style>
.dashboard {
    display: grid;
    grid-template-columns: 1fr 5fr;
    background-color: rgba(13, 0, 128, 0.26);
    height: 100vh;
    width: 100vw;
}
.content {
    background-color: white;
    border-radius: 5px;
    margin: 6px 6px 6px 0px;
}
</style>