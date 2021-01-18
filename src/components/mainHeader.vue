<template>
    <header>
        <img src="../assets/logo.svg" alt="">
        <p class="title">Туду</p>
        <button>Войти</button>
        <p class="nickname">Добро пожаловать, Евгений!</p>
    </header>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    header {
        background-color: #f3f3f5;
        display: inline-block;
        height: 80px;
        width: 100%;
        margin: 0px;
    }
    img {
        margin: 10px;
        height: 60px;
        float: left;
        width: 60px;
    }
    
    .title {
        margin-left: 30px;
        margin-top: 12px;
        color: #9c979d;
        font-size: 30pt;
        float: left;
    }
    .nickname {
        margin-right: 30px;
        font-weight: bold;
        margin-top: 25px;
        font-size: 15pt;
        float: right;
    }
    button {   
        background-color: #f2bf49;
        border-radius: 35px;
        margin-right: 30px;
        margin-top: 18px;
        display: inline; 
        font-size: 16pt;
        color: #fff;
        float: right;
        height: 40px;
        width: 100px;
        border: none;
    }

    button:hover {
        box-shadow: 0 0 10px rgba(58, 54, 54, 0.342);
    }

    button:focus {
        outline: none;
    }
</style>