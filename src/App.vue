<template>
    <div id="app">
<!--        <Login/>-->
        <Login2/>
    </div>
</template>

<script>
// import Login from "@/components/login/Login.vue";
import Login2 from "@/components/login/Login2.vue";
export default {
    name: 'App',
    components: {
        // Login,
        Login2,
    }
}
</script>

<style>
#app {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100vw;
    height: 100vh;
    background-color: #94bfb5;
}
</style>
