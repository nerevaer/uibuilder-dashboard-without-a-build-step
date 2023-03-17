<template>
    <div class="sidebar">
        <div class="title">
            Sidebar
        </div> 
        <div class="menu-items">
            <router-link to="/" custom v-slot="{ navigate }">
                <button @click="navigate" active-class="active" role="link" class="side-btn">
                    <div class="link-container">
                        Overview
                    </div>
                </button>
            </router-link>
            <router-link to="/messages" custom v-slot="{ navigate }">
                <button @click="navigate"  role="link" class="side-btn">
                    <div class="link-container">
                        Messages
                    </div>
                </button>
            </router-link>

            <!--
            <router-link to="/" active-class="active" tag="button" exact class="side-btn">
                <div class="link-container">
                    Overview
                </div>
            </router-link>

            <router-link to="/messages" active-class="active" tag="button" exact class="side-btn">
                <div class="link-container">
                    Messages
                </div>
            </router-link>
            -->
        </div>
    </div>
</template>


<style scoped>
.title {
    color: white;
    font-size: 24px;
    margin-top: 10px;
}
.menu-items {
    display: flex;
    flex-direction: column;
    margin-left: 6px;
}
.menu-items > * {
    margin-top: 20px;
}
.side-btn {
    border: none;
    padding: 16px 0px;
    cursor: pointer;
    font-size: 16px;
    font-weight: 500;
    color: white;
    background-color: transparent;
}
.side-btn :focus {
    outline: none;
}
.side-btn:active{
    position: relative;
    background-color: white;
    color: rgb(255, 174, 0);
    font-weight: 600;
    margin-left: 10px;
    border-radius: 5px 0 0 5px;
}

</style>