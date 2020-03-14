<template>
    <el-container class="home-container">
        <el-header>
            <div>
                <img src="../assets/heima.png" alt="">
                <span>电商后台管理系统</span>
            </div>
            <el-button type="info" @click="logout">退出</el-button>

        </el-header>
        <el-container>
            <el-aside>aside</el-aside>
            <el-main>min</el-main>
        </el-container>
    </el-container>
</template>

<script>
    export default {
        name: "Home",
        data() {

        },
        methods: {
            //退出系统，清除
            logout() {
                window.sessionStorage.clear()
                this.$router.push('/login')
            },
        }
    }
</script>

<style scoped>
    .home-container {
        height: 100%;
    }

    .el-header {
        background-color: #373d41;
        display: flex;
        justify-content: space-between;
        padding-left: 0;
        align-items: center;
        color: #fff;
        font-size: 20px;
    }

    .el-header div {
        display: flex;
        align-items: center;
    }

    .el-header span {
        margin-left: 15px;
    }

    .el-aside {
        background-color: #333744;
    }

    .el-aside .el-menu {
        border-right: none;
    }

    .el-main {
        background-color: #eaedf1;
    }

    .iconfont {
        margin-right: 10px;
    }

    .toggle-button {
        background-color: #4a5064;
        font-size: 10px;
        line-height: 24px;
        color: #fff;
        text-align: center;
        letter-spacing: 0.2em;
        cursor: pointer;
    }
</style>