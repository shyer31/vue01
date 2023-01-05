<template>
    <div class="container">
        <div class="register-box">
            <h2 class="register-title">
                <span>没有账号，去</span>注册
            </h2>
            <div class="input-box">
                <input type="text" placeholder="用户名">
                <input type="password" placeholder="密码">
                <input type="password" placeholder="确认密码">
            </div>
            <button>注册</button>
        </div>
        <div class="login-box slide-up">
            <div class="center">
                <h2 class="login-title">
                    <span>已有账号，去</span>登录
                </h2>
                <div class="input-box">
                    <input type="text" placeholder="用户名">
                    <input type="password" placeholder="密码">
                </div>
                <button>登录</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Login2"
}
</script>

<style scoped>
.container {
    width: 350px;
    height: 550px;
    border-radius: 15px;
    overflow: hidden;
    position: relative;
}
.container::after {
    content: "";
    position: absolute;
    inset: 0;
    background: url("@/assets/login.jpg") no-repeat;
    background-size: 500px;
    background-position: left bottom;
    opacity: .8;
}
.register-box {
    width: 70%;
    position: absolute;
    z-index: 1;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: .3s ease;
}
.register-title,
.login-title {
    color: #fff;
    font-size: 27px;
    text-align: center;
}
.register-title span,
.login-title span {
    color: rgba(0, 0, 0, .4);
    display: none;
}
.register-box .input-box,
.login-box .input-box {
    background-color: #fff;
    border-radius: 15px;
    overflow: hidden;
    margin-top: 50px;
    opacity: 1;
    visibility: visible;
    transition: .6s ease;
}
.register-box input,
.login-box input {
    width: 100%;
    height: 30px;
    border: none;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    font-size: 12px;
    padding: 8px 0;
    text-indent: 15px;
    outline: none;
}
.register-box input:last-child,
.login-box input:last-child {
    border-bottom: none;
}
.register-box input::placeholder,
.login-box input::placeholder {
    color: rgba(0, 0, 0, 0.4);
}
.register-box button,
.login-box button {
    width: 100%;
    padding: 15px 45px;
    margin: 15px 0;
    background: rgba(0, 0, 0, .4);
    border: none;
    border-radius: 15px;
    color: rgba(255, 255, 255, .8);
    font-size: 13px;
    font-weight: bold;
    cursor: pointer;
    opacity: 1;
    visibility: visible;
    transition: .3s ease;
}
.register-box button:hover,
.login-box button:hover {
    background-color: rgba(0, 0, 0, .8);
}

.login-box {
    position: absolute;
    inset: 0;
    top: 20%;
    z-index: 2;
    background-color: #fff;
    transition: .3s ease;
}
.login-box::before {
    content: "";
    background-color: #fff;
    width: 200%;
    height: 250px;
    border-radius: 50%;
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
}
.login-box .center  {
    width: 70%;
    position: absolute;
    z-index: 3;
    left: 50%;
    top: 40%;
    transform: translate(-50%, -50%);
}
.login-title {
    color: #000;
}
.login-box  .input-box {
    border: 1px solid rgba(0, 0, 0, .1);
}
.login-box button {
    background-color: #75a297;
}
.login-box.slide-up {
    top: 90%;
}
.login-box.slide-up .center {
    top: 10%;
    transform: translate(-50%, 0%);
}
.login-box.slide-up .login-title {
    font-size: 16px;
    cursor: pointer;
}
</style>