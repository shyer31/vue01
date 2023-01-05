<template>
    <el-card shadow="always" class="login-card">
        <h2>登录</h2>
        <el-form label-width="80px" :model="form" :rules="rules" ref="form">
            <el-form-item label="用户名" prop="username">
                <el-input v-model="form.username" placeholder="请输入用户名"></el-input>
            </el-form-item>
            <el-form-item label="密码" prop="password">
                <el-input placeholder="请输入密码" v-model="form.password" show-password></el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="onSubmit('form')">登录</el-button>
            </el-form-item>
        </el-form>
    </el-card>
</template>

<script>
export default {
    name: "Login",
    data() {
        return {
            form: {
                username: "",
                password: ""
            },
            rules: {
                username: [
                    {required: true, message: "请输入用户名", trigger: "blur"},
                    {min: 3, max: 5, message: "长度在3到5个字符", trigger: "blur"}
                ],
                password: [
                    {required: true, message: "请输入密码", trigger: "blur"},
                    {min: 3, max: 5, message: "长度在3到5个字符", trigger: "blur"}
                ]
            }
        }
    },
    methods: {
        onSubmit(formName) {
            this.$refs[formName].validate((valid) => {
                console.log(valid)
                if (valid) {
                    alert("submit!")
                } else {
                    console.log("error submit!")
                    return false
                }
            })
        }
    }
}
</script>

<style scoped>
.login-card {
    width: 450px;
    height: 260px;
}

.el-button {
    width: 50%;
}
</style>